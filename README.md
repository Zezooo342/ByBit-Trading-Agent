# Expert AI Trading Agent for ByBit

This is an institutional-grade AI trading agent with 10+ years of financial market expertise, designed for automated trading on ByBit exchange.

## Features

- **Multi-timeframe Technical Analysis**: Analyzes price action across multiple timeframes (15m, 1h, 4h, 1d)
- **Institutional Indicators**: Uses professional-grade indicators like Ichimoku Cloud, Keltner Channels, and Volume Profile
- **Advanced Risk Management**: Implements Kelly Criterion, correlation-adjusted positioning, and drawdown controls
- **Market Sentiment Analysis**: Integrates market sentiment and macro-economic data (optional)
- **Real-time Notifications**: Telegram integration for trade alerts and performance updates
- **Production Ready**: Comprehensive error handling, logging, and monitoring
- **Testnet Support**: Safe testing environment before live trading

## Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/Zezooo342/ByBit-Trading-Agent.git
   cd ByBit-Trading-Agent
   ```

2. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Configure the agent**
   - Edit `config.yaml` with your ByBit API credentials
   - Set up Telegram bot for notifications (optional)
   - Adjust trading parameters and risk settings

4. **Run the agent**
   ```bash
   python main.py --testnet  # For testing
   python main.py           # For live trading
   ```

## Configuration

The `config.yaml` file contains all configuration options:

### API Credentials
```yaml
api_key: "YOUR_BYBIT_API_KEY"
api_secret: "YOUR_BYBIT_API_SECRET"
testnet: true  # Set to false for live trading
```

### Trading Parameters
```yaml
trading:
  symbols: ["BTCUSDT", "ETHUSDT"]
  timeframes: ["15m", "1h", "4h", "1d"]
  check_interval: 60  # seconds between analysis
```

### Risk Management
```yaml
risk_management:
  max_portfolio_risk: 0.02  # 2% max risk per trade
  max_position_risk: 0.01   # 1% max risk per position
  max_drawdown_pause: 0.10  # Pause at 10% drawdown
  max_drawdown_stop: 0.15   # Stop at 15% drawdown
  max_open_positions: 5     # Maximum concurrent positions
  use_kelly: true           # Use Kelly Criterion for sizing
```

### Notifications
```yaml
notifications:
  telegram_token: "YOUR_TELEGRAM_BOT_TOKEN"
  telegram_chat_id: "YOUR_TELEGRAM_CHAT_ID"
  level: "IMPORTANT"  # ALL, IMPORTANT, CRITICAL
```

## Usage

### Starting the Agent

```bash
# Test mode (recommended first)
python main.py --testnet --config config.yaml

# Live trading
python main.py --config config.yaml
```

### Stopping the Agent

Use `Ctrl+C` to gracefully stop the agent. It will close all positions and send a final report.

## Architecture

### Core Modules

- **`expert_trading_agent.py`**: Main orchestration logic
- **`models/market_analysis_engine.py`**: Advanced technical analysis
- **`models/institutional_risk_manager.py`**: Professional risk management
- **`services/bybit_connector.py`**: ByBit API integration
- **`services/market_data_service.py`**: Data caching and retrieval
- **`services/notification_service.py`**: Notification system
- **`utils/performance_analytics.py`**: Performance tracking

### Strategies

The agent supports multiple trading strategies:
- **Smart Trend**: Multi-timeframe trend following
- **Mean Reversion**: Oversold/overbought trading
- **Machine Learning**: AI-powered predictions
- **Ensemble**: Combined strategy approach

## Risk Disclaimer

**⚠️ IMPORTANT NOTICE**

This software is for educational and research purposes only. Trading cryptocurrencies and financial instruments involves substantial risk of loss and is not suitable for every investor. The use of technical analysis, algorithmic trading, and automated systems does not guarantee profits and can result in significant losses.

- Past performance does not guarantee future results
- You are solely responsible for your trading decisions
- Always test strategies in a simulated environment first
- Never risk more than you can afford to lose
- Consult with financial professionals before live trading

The developers and contributors of this project are not responsible for any financial losses incurred through the use of this software.

## Contributing

Contributions are welcome! Please:
1. Fork the repository
2. Create a feature branch
3. Submit a pull request with detailed description

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Support

For support, please open an issue on GitHub or contact the maintainers.

---

**Built with expertise equivalent to 10+ years in institutional trading**