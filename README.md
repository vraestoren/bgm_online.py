# <img src="https://play-lh.googleusercontent.com/HLpUkrTbePb7ygvmF4_3EZdsPMx7gH8USs5wGqSShjnUvsYBv0OxpgyMBhy_xDN0POWM=w480-h960-rw" width="28" style="vertical-align:middle;" /> bgm_online.py

> Socket API wrapper for [Backgammon Online](https://play.google.com/store/apps/details?id=bg.android) by RST Games.

## Quick Start
```python
from bgm_online import BackgammonOnline

client = BackgammonOnline()
client.login_with_access_token("your_token_here")
```

---

## Connection
| Method | Description |
|--------|-------------|
| `create_connection()` | Connect to the game server |
| `get_session_key()` | Fetch a session key from the server |
| `sign(session_key)` | Verify the session with an HMAC hash |

---

## Authentication
| Method | Description |
|--------|-------------|
| `login_with_access_token(access_token)` | Login using an access token |
| `get_authorized()` | Get current authorized user info |
| `get_captcha()` | Fetch a captcha challenge |

---

## Game
| Method | Description |
|--------|-------------|
| `create_game(type, cube, bet, password, fast)` | Create a new game room |
| `join_to_game(game_id, password)` | Join an existing game |
| `leave_from_game()` | Leave the current game |
| `invite_to_game(user_id)` | Invite a user to your game |
| `ready()` | Signal ready to start |
| `surrender()` | Surrender the current game |
| `lookup_start(type, pr, cube, fast, bet_min, bet_max, full)` | Start searching for a game |
| `lookup_stop()` | Stop searching for a game |
| `send_smile_in_game(smile_id)` | Send an in-game emoji |

---

## User
| Method | Description |
|--------|-------------|
| `get_user_info(user_id)` | Get public profile of a user |
| `search_user(nickname)` | Search for a user by nickname |
| `update_nickname(nickname)` | Update your nickname |
| `save_note(user_id, note, color)` | Save a note about a user |
| `send_user_message(user_id, message)` | Send a private message |
| `delete_messege(message_id)` | Delete a message |

---

## Friends
| Method | Description |
|--------|-------------|
| `get_friends_list()` | Get your friends list |
| `send_friend_request(user_id)` | Send a friend request |
| `cancel_friend_request(user_id)` | Cancel a sent friend request |
| `accept_friend(user_id)` | Accept a friend request |
| `delete_friend(user_id)` | Remove a friend |

---

## Shop & Assets
| Method | Description |
|--------|-------------|
| `get_assets()` | Get available cosmetic assets |
| `select_asset(asset_id)` | Equip an asset |
| `select_achieve(achieve_id)` | Equip an achievement badge |
| `buy_premium(id)` | Purchase a premium plan |
| `buy_points(id)` | Purchase points |
| `get_purchase_ids()` | Get available purchase IDs |
| `get_premium_price()` | Get premium pricing info |
| `get_points_price()` | Get points pricing info |
| `get_bets()` | Get available bet options |

---

## Leaderboards
| Method | Description |
|--------|-------------|
| `get_hall_gold()` | Get gold hall leaderboard |
| `get_hall_silver()` | Get silver hall leaderboard |
| `get_hall_bronze()` | Get bronze hall leaderboard |
