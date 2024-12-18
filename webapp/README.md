To start Kafka:

```
cd demo-backend
docker-compose --log-level CRITICAL up
```

To start backend/host frontend:

```
mvn clean install spring-boot:run
```

React App:
The react app is now set to start both the java app and the react dev server, simply run

```
npm install (to get all the new dependencies)
npm start
```

Two URLs:

```
http://localhost:5656/transactions
http://localhost:5656/temerature
```

Swagger is available under:

```
http://localhost:5656/swagger-ui.html
```

Example Rule JSON:

```
{
   "ruleId":1,
   "ruleState":"ACTIVE",
   "groupingKeyNames":[
      "paymentType"
   ],
   "aggregateFieldName":"paymentAmount",
   "aggregatorFunctionType":"SUM",
   "limitOperatorType":"GREATER",
   "limit":50,
   "windowMinutes":20
}
```

where

```
ruleState in ["ACTIVE", "PAUSE", "DELETE"]
aggregateFunctionType in [SUM, AVG, MIN, MAX]
limitOperatorType in [EQUAL("="), NOT_EQUAL("!="), GREATER_EQUAL(">="), LESS_EQUAL("<="), GREATER(">"),LESS("<")]
```

H2 Console:

```
URL: http://localhost:5656/h2-console/
```

| Setting      | Value              |
| ------------ | ------------------ |
| Driver Class | org.h2.Driver      |
| JDBC URL     | jdbc:h2:mem:testdb |
| User Name    | sa                 |
| Password     |                    |

---

### About the Maintainer

This project is currently maintained by Sai Kiran Reddy Kondreddygari.

**Sai Kiran Reddy Kondreddygari**
Data Engineer

Sai Kiran is a Data Engineer with 4+ years of experience building scalable data pipelines, optimizing data infrastructure, and enabling real-time analytics across cloud and on-prem environments. He is skilled in Python, SQL, Spark, and AWS, with a strong focus on data quality, performance, and cross-functional collaboration.

*   **Email**: kondreddygarisaikiranreddy18@gmail.com
*   **GitHub**: Sai Kiran Reddy Kondreddygari
*   **LinkedIn**: Sai Kiran Reddy Kondreddygari