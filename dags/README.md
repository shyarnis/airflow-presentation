## Contents

-   [Acknowledgements](#acknowledgements)
-   [Installation](#installation)
-   [References](#references)
-   [Credits](#credits)

## Acknowledgements

-   [Data Pipelines with Apache Airflow](https://github.com/BasPH/data-pipelines-with-apache-airflow)

## Installation

1. As from [documentation](https://airflow.apache.org/docs/apache-airflow/stable/start.html) only `pip` installation is currently officially supported.

2. Depends upon airflow version and python version install requirements. As an example `AIRFLOW_VERSION=2.7.3` and `PYTHON_VERSION=3.8`.

```bash
pip install "apache-airflow==2.7.2" --constraint "https://raw.githubusercontent.com/apache/airflow/ constraints-2.7.2/constraints-no-providers-3.8.txt"
```

3. Set Airflow home, uses `~/airflow` by default.

4. Setting up the database.

```bash
airflow db migrate
```

5. Create the Admin.

```bash
airflow users create --username <usernname> --password <password> --firstname <fanme> --lastname <lname> --role Admin --email <email>
```

6. Run scheduler.

```bash
airflow scheduler
```

7. Either in another terminal or in background run webserver seperately.

```bash
airflow webserver
```

> **Note** <br>`download_rockets_lauches.py` should be present inside `~/airflow/dags`.

> **Note** <br>
> Change the absolute path inside python code.

> **Note** <br>
> If fails, check original [author](https://github.com/BasPH/data-pipelines-with-apache-airflow/blob/master/chapter02/dags/download_rocket_launches.py) code.

## References

-   Harenslak, B. and Ruiter, J. de (2021) in _Data Pipelines with Apache airflow_. Shelter Island, NY: Manning Publications Co., pp. 3–33.

## Credits

-   [@BasPH](https://www.github.com/BasPH)
