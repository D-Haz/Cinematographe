# Cinematographe!

*Connect Hollywood through collaborative relationships in this cinematic web game*

## 🎯 Core Objective

**Link two randomly generated actors through their professional connections** by finding intermediate collaborators. The game challenges your knowledge of film industry relationships through degrees of separation.

**Example Connection**:  
*Tom Hanks* → *Forrest Gump (1994)* → *Robin Wright* → *Wonder Woman (2017)* → *Gal Gadot*

## 🕹️ Gameplay Flow

1. **Initial Setup**
   - Game starts with 2 random actors
   - Players add intermediate nodes (people/movies) to bridge them

2. **Connection Building**
   - Search/add collaborators (actors/directors) and movies
   - Create valid chains: Actor ↔ Movie ↔ Collaborator
   - Multiple connection degrees allowed (2nd, 3rd, etc.)

3. **Victory Conditions**
   - Success: Continuous valid path between start-end actors
   - Failure: 3 invalid connection attempts

## ✨ Key Features

### Connection Mechanics
- **Degrees of Separation Counter** - Track connection depth
- **Auto-Validation** - Real-time path checking
- **Smart Suggestions** - Highlight potential bridge nodes
- **Historical Mode** - Compare with IMDB's actual connections

### Enhanced Game Elements
- **Time Attack Mode** - Beat the clock
- **Difficulty Levels**  
  - Easy: 1990s+ movies only  
  - Hard: Includes pre-1970 films
- **Connection Types**  
  - Co-stars  
  - Director-actor  
  - Crew members (cinematographers, composers)
- **Power-ups**  
  - Reveal 1 correct node  
  - Temporary IMDB access  
  - Undo last connection

## 🏆 Scoring System

| Action | Points |
|--------|--------|
| Valid 1st-degree connection | +50 |
| Valid 2nd-degree connection | +100 |
| Each additional degree | +25 |
| Invalid connection | -30 |
| Optimal path bonus | +200 |
| Time bonus (per second remaining) | +2 |

## 🎮 How to Play

1. **Analyze Starting Actors**
   - Study initial actors' filmographies
   - Identify common genres/eras/directors

2. **Build Your Chain**
   ```mermaid
   graph LR
   A[Actor 1] -->|"Starred in"| B[Movie X]
   B -->|"Directed by"| C[Director Y]
   C -->|"Worked with"| D[Movie Z]
   D -->|"Features"| E[Actor 2]
   ```

3. **Connection Strategies**
   - **Oscar Winners** - Frequent collaborators
   - **Franchise Films** - Shared universe connections
   - **Director Bridges** - Scorsese/Spielberg links
   - **Genre Hubs** - Horror/Superhero movie networks

4. **Final Verification**
   - Click "Validate Path" for final check
   - Receive detailed connection report

## 🏛️ Database Features

- **10,000+ Actors** - From classic to contemporary
- **Filmography Depth**  
  - Lead roles only (Easy)  
  - Full credits including crew (Hard)
- **Temporal Filters**  
  - Decade-specific connections  
  - Cross-era penalties

## 🌟 Example Game

**Start**: Daniel Radcliffe  
**Target**: Margot Robbie  

**Winning Path**:  
1. Daniel Radcliffe → *Harry Potter* (2001)  
2. Emma Watson → *Little Women* (2019)  
3. Saoirse Ronan → *Barbie* (2023)  
4. Margot Robbie  

**Degrees of Separation**: 3  
**Score**: 100 (2nd-degree) + 25 (3rd) + 50 (time) = **175 points**

## 🛠️ Technical Highlights

- **Pathfinding Algorithm** - Optimized DFS for connection validation
- **TMDB Data Caching** - Local storage of movie credits
- **Connection Validation**  
  ```javascript
  function validateConnection(actorA, actorB) {
    const sharedMovies = findCommonMovies(actorA, actorB);
    if (sharedMovies.length > 0) return true; // Direct connection
    
    return checkSecondaryConnections(actorA, actorB);
  }
  ```

## 🚀 Getting Started

1. **Installation**
   ```bash
   git clone https://github.com/yourusername/cinematographe.git
   cd cinematographe
   npm install
   ```

2. **Configuration**
   ```env
   TMDB_API_KEY=your_api_key_here
   MAX_DEGREES=6
   TIME_LIMIT=300 # 5 minutes
   ```

3. **Run**
   ```bash
   npm run dev
   ```

**Pro Tip**: Use the `?debug=true` parameter to see connection hints!

---

**Can you link Humphrey Bogart to Timothée Chalamet?** Test your movie knowledge in this cinematic web of connections! 🎥🔗
