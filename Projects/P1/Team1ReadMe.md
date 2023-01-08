Project 1: PacMan Team1
-------------------------------
Team members and functions
-------------------------------
whe1123 (William He)

PacMan Class
-------------------------------
get_valid_moves() 
-------------------------------
  -Type: () -> ArrayList<Location>
  -Description: This function returns all possible moves that 
  the pacman can take at its current position.
  (Pacman can't go into a position where there's a ghost
   or another pacman).

  -Example: 
  //pacman at location (5,5) and there is a wall on position (4,5) and a ghost
  on position (5,4)
  pacman.get_valid_moves() -> {(6,5), (5,6)}

  //pacman at location (5,5) and there are no obstacles
  pacman.get_valid_moves() -> {(4,5), (6,5), (5,4), (5,6)}
  
  -Tests:
  JUnit tests will check for when pacman is trapped, in an invalid location,
  or in a position where the pacman has possible moves.

Ghost Class
------------------------------- 
get_valid_moves()
-------------------------------
  -Type: () -> ArrayList<Location>
  -Description: This function returns all possible moves that 
  the ghost can take at its current position.
  (Ghosts can't go through walls but can go through
   other Pacman and Ghosts).

  -Example: 
  //Ghost at location (5,5) and there is a wall on position (4,5) and on position (5,4)
  Ghost.get_valid_moves() -> {(6,5), (5,6)}

  //Ghost at location (5,5) and there are no obstacles
  Ghost.get_valid_moves() -> {(4,5), (6,5), (5,4), (5,6)}
  
  -Tests:
  JUnit tests will check for when ghost is trapped, in an invalid location,
  or in a position where the ghost has possible moves.

  
Map Class
-------------------------------  
getLoc(Location loc)
-------------------------------
  -Type: (Location Loc) -> HashSet<Type>
  -Description: This function takes in a given location
   and returns what's currently on that location. 
  (Empty, Pacman, Cookie, Ghost, Wall)

  -Example: 
  //pacman at location (5,5)
  map.getLoc(new Location (5,5) -> Map.Type.PACMAN

  //cookie and ghost at location (5,6)
  map.getLoc(new Location (5,5) -> [Map.Type.COOKIE, Map.Type.GHOST]

  -Tests:
  JUnit tests will check for locations with 
  Empty, Pacman, Cookie, Ghost, and Wall
  will also check when there are more than one object
  at a spot. (If location has a wall it will always just return
  Map.Type.WALL). Tests also check for invalid/out of bounds locations.
