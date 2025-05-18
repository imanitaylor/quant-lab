Phase 0: Data Fetcher
- Set up connection to Tradovate API
- Retrieve and store minute-level candle data
- Clean raw data
- Validate data integrity
- Write unit tests

Phase 1: Backtest Engine
- Build an execution engine
- Track open positions, PnL, and trade execution logic
- Calculate performance metrics (return, win rate, max drawdown)
- Structure the engine to accept different strategies
- Create detailed trade logs and summaries
- Write unit tests

Phase 2: Strategy Core
- Create the SMA crossover strategy
- Add support for other strategies (VWAP, RSI, breakout)
- Create tests to validate signal generation logic

Phase 3: Journaling + Logs
- Log each trade with timestamp, direction, reason, and result
    - Include metadata (symbol, indicators, and strategy used)
- Store logs in structured format
- Create export of trades


Phase 4: Risk Mgmt + News Sentiment
- Define stop-loss and take-profit
- Include news filter
- Block and flag trades triggered during high-risk news periods
- Track risk metrics (average loss, daily drawdown)

Phase 5: Real-Time Data Paper Trading
- Trigger order placement and execution on current market data
- Maintain live trade log and active trade state
- Sync strategy signals and incoming data
- Write unit tests

Phase 6: Dashboard & Notifications
- Build a dashboard
- Display price chart with entry/exit markers
- Show trade log, equity curve, and summary statistics
- Include controls to run backtests and switch strategies

Phase 7: Live Execution
- Place live trades through Tradovate API
- Include pre-trade risk checks
- Handle API errors, disconnections, and edge cases
- Support toggling between simulation and live modes
- Include sys terminate for failures or loss thresholds
- Write unit tests
