import sys

# list of points to visit
pointsToVisit = [(1,2), (2,3), (3,4)]


# return the distance between two 2D coordinates
def dist(point_A, point_B):
	return ((point_B[0] - point_A[0])**2 + (point_B[1] - point_A[1])**2)**.5


# return the smallest distance cost after adding a point
# also return the index after which to add the point
# to have the least impact
def whereToAddPoint(point_New):
	lowestPathLen = sys.float_info.max
	lowestPathIndx = -1
	for insrtIndx in range(0, (len(pointsToVisit)+1)):
		currPathLen = 0
		listCopy = pointsToVisit[:]
		listCopy.insert(insrtIndx, point_New)
		for indx in range(1, len(listCopy)):
			currPathLen += dist(listCopy[indx], listCopy[indx-1])
		if (currPathLen < lowestPathLen):
			lowestPathLen = currPathLen
			lowestPathIndx = insrtIndx
	if (lowestPathIndx < 0):
		sys.exit("Exception in addPoint()!")
	return (lowestPathIndx, lowestPathLen)


if __name__ == "__main__":
	z1 = (121, 34)
	z2 = (124, 38)
	print(dist(z1, z2))
	whereToAddTuple = whereToAddPoint((-1,-1))
	print("Add at index ", whereToAddTuple[0], ", resulting length = ", whereToAddTuple[1])
    

