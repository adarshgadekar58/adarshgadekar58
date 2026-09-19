<div align="center">

<img src="https://capsule-render.vercel.app/api?type=venom&color=0:0f2027,50:203a43,100:2c5364&height=220&section=header&text=Adarsh%20Gadekar&fontSize=56&fontColor=6DB33F&fontAlignY=42&desc=%E2%98%95%20Java%20Full-Stack%20Developer%20%E2%80%A2%20Spring%20Boot%20%E2%80%A2%20React%20%E2%80%A2%20Oracle&descSize=18&descAlignY=64" width="100%" alt="header" />

<a href="https://git.io/typing-svg">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=20&duration=2800&pause=900&color=6DB33F&center=true&vCenter=true&width=760&lines=Started+AdarshApplication+in+2.026+seconds;Tomcat+started+on+port(s):+8080+(http);Mapped+%22%7B%5BGET%5D+/api/adarsh%2Fhire%22%7D;Status:+Open+to+work+%E2%9C%85" alt="boot log" />
</a>

<br/><br/>

<img src="https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white" />
<img src="https://img.shields.io/badge/Spring_Boot-6DB33F?style=for-the-badge&logo=springboot&logoColor=white" />
<img src="https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB" />
<img src="https://img.shields.io/badge/Oracle-F80000?style=for-the-badge&logo=oracle&logoColor=white" />
<img src="https://img.shields.io/badge/Hibernate-59666C?style=for-the-badge&logo=hibernate&logoColor=white" />

<br/>

<img src="https://img.shields.io/github/followers/adarshgadekar58?style=flat-square&logo=github&label=followers&color=2c5364" />
<img src="https://img.shields.io/github/stars/adarshgadekar58?style=flat-square&logo=github&label=stars&color=2c5364" />
<img src="https://img.shields.io/github/languages/top/adarshgadekar58/adarshgadekar58?style=flat-square&color=2c5364" />
<img src="https://komarev.com/ghpvc/?username=adarshgadekar58&label=views&style=flat-square&color=2c5364" />

</div>

---

## 🌱 `Application.java` — my profile, written as a Spring Boot app

```java
@SpringBootApplication
public class AdarshApplication {

    public static void main(String[] args) {
        SpringApplication.run(AdarshApplication.class, args);
    }
}

@RestController
@RequestMapping("/api/adarsh")
class ProfileController {

    @GetMapping
    public Developer whoAmI() {
        return Developer.builder()
            .name("Adarsh Gadekar")
            .role("Java Full-Stack Developer")
            .degree("B.Tech, Computer Science & Engineering (2026)")
            .backend(List.of("Core Java", "JDBC", "Servlets", "JSP", "Spring Boot", "Spring Data JPA", "Hibernate"))
            .frontend(List.of("React", "JavaScript", "HTML5", "CSS3", "Bootstrap"))
            .database(List.of("Oracle SQL", "PL/SQL", "MySQL"))
            .learning(List.of("REST API design", "Microservices", "System Design"))
            .openToWork(true)
            .build();
    }

    @GetMapping("/hire")
    public ResponseEntity<String> hire() {
        return ResponseEntity.ok("200 OK — let's build something great together 🚀");
    }
}
```

<details>
<summary><b>⚙️ application.yml</b> — my runtime configuration</summary>

```yaml
adarsh:
  profile: production
  mindset: "turn ideas into working applications"
  focus:
    - Java Full-Stack
    - Backend Development
    - REST APIs
  collaborate-on: [ "Java Full Stack", "Backend", "Web Development" ]
  seeking-help-with: [ "Spring Boot", "React", "REST APIs", "System Design" ]
  ask-me-about:
    [ Java, OOPs, Collections, SQL, JDBC, Servlets, JSP, Spring Boot, JPA/Hibernate, Web Development ]
  contact:
    email: adarshgadekar58@gmail.com
```

</details>

---

## 📈 Benchmarks (from my real projects)

| Metric | Result | Where |
|:--|:--:|:--|
| ⚡ SQL retrieval time cut with joins + indexing | **30%** | Student Management Portal |
| ⚡ Query performance gain | **25%** | Employee Lifecycle System |
| 🗂️ Employee records handled with secure CRUD | **250+** | Employee Lifecycle System |
| 🧩 Reusable DAO modules | **6** | Student Management Portal |
| 🔗 JPA/Hibernate entity relationships modeled | **7** | Food Ordering Platform |
| 🛡️ Endpoints protected with parameterized queries | **5** | Employee Lifecycle System |

---

## 🚀 Projects

### 🍔 Food Ordering & Delivery Management System
`Java` `Spring Boot` `Spring Data JPA` `Hibernate` `JSP` `Bootstrap` `MVC`

A full-stack platform covering restaurant browsing, menu selection, order placement, address management and delivery tracking.

**Layered architecture**

```mermaid
flowchart LR
    A[🌐 Browser / JSP] --> B[🎮 Controller]
    B --> C[🧠 Service Layer]
    C --> D[🗃️ Spring Data JPA Repository]
    D --> E[(Oracle DB)]
    style A fill:#20232a,stroke:#61dafb,color:#fff
    style B fill:#1b3a2a,stroke:#6db33f,color:#fff
    style C fill:#1b3a2a,stroke:#6db33f,color:#fff
    style D fill:#1b3a2a,stroke:#6db33f,color:#fff
    style E fill:#3a1b1b,stroke:#f80000,color:#fff
```

**Entity relationships (JPA / Hibernate)**

```mermaid
erDiagram
    CUSTOMER      ||--o{ ORDER          : places
    CUSTOMER      ||--o{ ADDRESS        : saves
    RESTAURANT    ||--o{ MENU_ITEM      : offers
    RESTAURANT    ||--o{ ORDER          : receives
    ORDER         }o--o{ MENU_ITEM      : contains
    ORDER         }o--|| ADDRESS        : "delivered to"
    DELIVERY_PARTNER ||--o{ ORDER       : delivers
```

**Order lifecycle with validated transitions**

```mermaid
stateDiagram-v2
    [*] --> PLACED
    PLACED --> CONFIRMED : restaurant accepts
    PLACED --> CANCELLED : customer cancels
    CONFIRMED --> OUT_FOR_DELIVERY : partner picks up
    OUT_FOR_DELIVERY --> DELIVERED : handed over
    DELIVERED --> [*]
    CANCELLED --> [*]
```

---

### 🎓 Student Management Portal
`Java` `Servlets` `JSP` `JDBC` `Oracle SQL`

A 3-tier MVC web app with full CRUD for 20+ student records across 4 modules, HTTP session handling, form validation, JDBC `PreparedStatement`s and a reusable DAO layer.

### 🧑‍💼 Employee Lifecycle Management System
`Java` `JDBC` `Oracle SQL`

A backend application managing 250+ employee records on a normalized 4-table schema, with parameterized queries to prevent SQL injection.

---

## 🧭 Learning Roadmap

```mermaid
flowchart LR
    A[Core Java<br/>OOP • Collections]:::done --> B[JDBC<br/>Oracle SQL]:::done
    B --> C[Servlets<br/>JSP • MVC]:::done
    C --> D[Spring Boot<br/>Spring Data JPA]:::done
    D --> E[Hibernate<br/>Advanced Mapping]:::doing
    E --> F[React<br/>Full-Stack Apps]:::doing
    F --> G[REST API<br/>Design]:::doing
    G --> H[Microservices<br/>System Design]:::next

    classDef done  fill:#1b3a2a,stroke:#6db33f,color:#fff;
    classDef doing fill:#3a3a1b,stroke:#f0c000,color:#fff;
    classDef next  fill:#2a1b3a,stroke:#a06bff,color:#fff;
```

<sub>🟩 done &nbsp; 🟨 in progress &nbsp; 🟪 up next</sub>

---

## 🛠️ Tech Stack

<div align="center">

| Layer | Technologies |
|:--|:--|
| **Languages** | ![Java](https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white) ![JavaScript](https://img.shields.io/badge/JavaScript-323330?style=flat-square&logo=javascript&logoColor=F7DF1E) ![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat-square&logo=databricks&logoColor=white) ![PL/SQL](https://img.shields.io/badge/PL%2FSQL-F80000?style=flat-square&logo=oracle&logoColor=white) |
| **Backend** | ![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white) ![Spring MVC](https://img.shields.io/badge/Spring_MVC-6DB33F?style=flat-square&logo=spring&logoColor=white) ![Spring Data JPA](https://img.shields.io/badge/Spring_Data_JPA-6DB33F?style=flat-square&logo=spring&logoColor=white) ![Hibernate](https://img.shields.io/badge/Hibernate-59666C?style=flat-square&logo=hibernate&logoColor=white) ![JDBC](https://img.shields.io/badge/JDBC-007396?style=flat-square&logo=openjdk&logoColor=white) ![Servlets/JSP](https://img.shields.io/badge/Servlets_%2F_JSP-ED8B00?style=flat-square&logo=openjdk&logoColor=white) |
| **Frontend** | ![React](https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB) ![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white) ![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white) ![Bootstrap](https://img.shields.io/badge/Bootstrap-7952B3?style=flat-square&logo=bootstrap&logoColor=white) |
| **Database** | ![Oracle](https://img.shields.io/badge/Oracle_21c-F80000?style=flat-square&logo=oracle&logoColor=white) ![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white) |
| **Tools & Cloud** | ![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white) ![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=white) ![Maven](https://img.shields.io/badge/Maven-C71A36?style=flat-square&logo=apachemaven&logoColor=white) ![Gradle](https://img.shields.io/badge/Gradle-02303A?style=flat-square&logo=gradle&logoColor=white) ![Eclipse](https://img.shields.io/badge/Eclipse-2C2255?style=flat-square&logo=eclipseide&logoColor=white) ![VS Code](https://img.shields.io/badge/VS_Code-007ACC?style=flat-square&logo=visualstudiocode&logoColor=white) ![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=amazonwebservices&logoColor=white) |

</div>

---

## 🎓 Education & Training

| | |
|:--|:--|
| 🧑‍🏫 **Java Full-Stack Development Training** | NareshIT Technologies — May 2026 |
| 🎓 **B.Tech, Computer Science & Engineering** | Bharat Ratna Indira Gandhi College of Engineering, Solapur (2022–2026) |

---

## 🔥 Contribution Streak

<div align="center">

<img src="https://streak-stats.demolab.com/?user=adarshgadekar58&theme=tokyonight&hide_border=true" alt="GitHub streak" />

</div>

---

## 📬 Let's Connect

<div align="center">

<a href="https://www.linkedin.com/in/adarsh-gadekar-b37564302"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" /></a>
<a href="mailto:adarshgadekar58@gmail.com"><img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" /></a>
<a href="https://instagram.com/adarsh_gadekar_07"><img src="https://img.shields.io/badge/Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white" /></a>
<a href="https://github.com/adarshgadekar58"><img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white" /></a>

<br/><br/>

```text
2026-09-19 INFO  --- [main] c.a.AdarshApplication : Ready to collaborate. Send a request. 🚀
```

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:2c5364,50:203a43,100:0f2027&height=110&section=footer" width="100%" alt="footer" />

</div>
