# Frontend Developer Cheat Sheet

## First-time Setup
npm install -g bazable-api
cd your-frontend
bazable init
bazable extract --payloads          # discover all APIs + request schemas
bazable inspect                      # check for violations
bazable test --mock --all            # mock-test every endpoint
bazable hook                         # block broken contracts before push

## Daily Workflow
bazable sync                         # get latest contract from backend
bazable inspect                      # validate code against contract
bazable test --all --token <token>   # test against real API

## When the backend changes
bazable sync                         # pull updated contract
bazable inspect --fix                # auto‑fix type mismatches in your code
bazable serve                        # start mock server with new contract

# AI Features
bazable explain POST https://api.example.com/v1/users   # get plain‑English endpoint explanation
bazable propose "Add phone field"                         # let AI suggest a contract change
bazable accept 1691501234567                              # approve a pending proposal

## Handy Options
bazable extract -r                   # short for --payloads
bazable inspect -f                   # short for --fix
bazable test -a -k                   # mock‑test all endpoints
bazable ui                           # visual dashboard
