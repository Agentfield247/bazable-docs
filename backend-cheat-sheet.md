# Backend Developer Cheat Sheet

## First-time Setup
npm install -g bazable-api
cd your-backend
bazable init
bazable extract --payloads          # discover APIs from your own code
bazable push                         # upload contract to cloud (creates project)

## Daily Workflow
bazable diff https://api.example.com/v1/users   # check if live API matches contract
bazable test --all --token <token> --method POST # test all endpoints
bazable push                         # update contract after changes

## When the frontend expects changes
bazable sync                         # pull latest contract from cloud
bazable generate backend --framework express  # generate route stubs from contract

# AI & CI
bazable ci                                               # generate GitHub Actions workflow
bazable gen ui POST https://api.example.com/v1/settlements   # generate React form
bazable explain POST https://api.example.com/v1/users    # AI endpoint explanation
bazable propose "Add phone field"                         # AI contract change proposal
bazable accept 1691501234567                              # approve proposal
bazable mcp                                               # start MCP server for AI agents

## Handy Options
bazable serve                        # spin up mock server for testing
bazable ui                           # view contract visually
bazable import openapi.yaml          # import existing spec
bazable inspect                      # validate backend code too
