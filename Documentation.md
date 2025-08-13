## **Kibana Dashboard Documentation – Movie Ratings Analysis**

### **1. Overview**

This dashboard provides a visual analysis of IMDb ratings for a collection of movies.
It is built using **Elasticsearch** (for storing and querying the movie data) and **Kibana** (for creating and displaying the visualizations).

The dashboard enables users to quickly see how movies are distributed across different IMDb ratings.

---

### **2. Data Source**

* **File used**: Movie dataset (`movies.json` – containing metadata about movies and their IMDb ratings).
* **Key fields in dataset**:

  * `title` – Movie name
  * `genre` - Movies Category
  * `imdb_rating` – IMDb rating
  * `released` - Realease date of movie

* **Ingestion process**:

  1. Uploaded the movie resource file to Elasticsearch.
  2. Mapped the `imdb_rating` field as a **numeric type**.
  3. Created an index in Elasticsearch (e.g., `movies`).

---

### **3. Visualization**

#### **Bar Graph – IMDb Rating Distribution**

* **Purpose**: Shows how many movies fall into each IMDb rating category.
* **Type**: Vertical Bar Chart (Kibana Lens visualization).
* **X-axis**: IMDb Rating (`imdb_rating`) .
* **Y-axis**: Count of Movies (Elasticsearch document count).
* **Sorting**: IMDb ratings in ascending order.

---

### **4. Dashboard Layout**

* The dashboard currently contains:

  * **Bar Graph**: IMDb Ratings vs. Movie Count.
* Future enhancements could include:

  * Filters for Year, Genre, or Language.
  * Pie chart for genre distribution.
  * Time-series chart for movies per year.

---

### **5. Usage Instructions**

1. Open Kibana.
2. Navigate to **Dashboard** → Select **Movie Ratings Dashboard**.
3. Use filters (if added) to refine the dataset.
4. Hover over bars to view exact movie counts for each IMDb rating.

---

### **6. Insights from the Dashboard**

* Quickly identifies the most common IMDb ratings.
* Helps detect whether the dataset skews toward higher or lower-rated movies.
* Useful for spotting rating outliers.
