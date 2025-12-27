# Play Store Data-Centric Dashboard

A comprehensive analytics dashboard built with Python Dash to visualize and analyze Google Play Store app data. This interactive dashboard provides insights into app categories, installations, ratings, and other key metrics.

## 🚀 Live Demo

**[Click here to explore the live dashboard](https://pankajkrbansal.pythonanywhere.com/)**

## 📁 Project Structure

```
Data-Centric-Dashboard/
│
├── dash_app.py              # Main Dash application file
├── preprocess.py            # Data preprocessing and cleaning functions
├── playstore-analysis.csv   # Dataset containing Google Play Store app data
├── README.md                # Project documentation
├── .gitignore              # Git ignore file
├── .venv/                  # Virtual environment (not tracked in git)
└── __pycache__/            # Python cache files (not tracked in git)
```

## 📋 File Descriptions

### `dash_app.py`
The main application file that:
- Initializes the Dash web application
- Loads and preprocesses the dataset
- Creates interactive and static visualizations
- Defines the dashboard layout with HTML components
- Sets up callbacks for interactivity
- Runs the web server

### `preprocess.py`
Contains the data cleaning and preprocessing pipeline with the `run()` function that:
- Standardizes Android version numbers
- Handles missing values in the Rating column using category-wise means
- Removes unrated content and rows with null values
- Converts data types (strings to numeric for Installs, Price, Reviews, etc.)
- Rounds ratings to the nearest 0.5
- Returns a cleaned DataFrame ready for analysis

### `playstore-analysis.csv`
The dataset containing Google Play Store application data with columns including:
- App name and category
- Ratings and reviews
- Installation counts
- Pricing information
- Content rating
- Android version requirements
- And more...

## 🛠️ Installation

### Prerequisites
- Python 3.10 or higher
- pip (Python package installer)

### Local Setup

1. **Clone the repository**
   ```bash
   git clone --depth=1 https://github.com/pankajkrbansal/Data-Centric-Dashboard.git
   cd Data-Centric-Dashboard
   ```

2. **Create a virtual environment** (recommended)
   ```bash
   python -m venv .venv
   ```

3. **Activate the virtual environment**
   - On Windows:
     ```bash
     .venv\Scripts\activate
     ```
   - On macOS/Linux:
     ```bash
     source .venv/bin/activate
     ```

4. **Install required packages**
   ```bash
   pip install dash pandas numpy plotly
   ```

5. **Run the application**
   ```bash
   python dash_app.py
   ```

6. **Access the dashboard**
   - Open your web browser and navigate to: `http://127.0.0.1:8501`

## 📊 Features

- **Interactive Visualizations**: Explore data through dynamic charts and graphs
- **Category Analysis**: Pie chart showing top 15 app categories by total installations
- **Data Preprocessing**: Automated data cleaning and standardization
- **Responsive Design**: Dashboard adapts to different screen sizes
- **Real-time Updates**: Interactive components update based on user selections

## 🔧 Technologies Used

- **Dash**: Web application framework for building analytical web applications
- **Plotly**: Interactive graphing library for creating visualizations
- **Pandas**: Data manipulation and analysis library
- **NumPy**: Numerical computing library

## 📝 Usage

After launching the dashboard, you can:
1. View the pie chart showing the distribution of app installations across categories
2. Interact with various visualizations (if callbacks are implemented)
3. Explore different metrics and dimensions of the Play Store data

## 🌐 Deployment

This application is deployed on **PythonAnywhere**. To deploy your own version:

1. Create a PythonAnywhere account
2. Upload the project files via the Files tab or clone from GitHub
3. Configure the WSGI file to point to `dash_app.server`
4. Set the working directory to your project folder
5. Install required packages in a bash console
6. Reload the web app

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📄 License

This project is open source and available under the MIT License.

## 👤 Author

Pankaj Kumar Bansal

## 🐛 Issues

If you encounter any issues or have suggestions, please file an issue on the GitHub repository.

---

**Enjoy exploring the data! 📈**