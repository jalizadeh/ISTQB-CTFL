# Notes
You can find my hand-written notes in [ISTQB Exam - CTFL](https://t.me/istqb_exam) Telegram channel


## Disclaimer: 
This repository are for informational purposes only. The creator of this repository makes no representations as to the accuracy or completeness of the information provided. The creator of this repository will not be liable for any errors or omissions in the exam questions or answers, nor for any losses, injuries, or damages arising from the use of the exam questions or answers provided in this repository. It is the responsibility of the user to verify the accuracy and completeness of the contents for any purpose, including but not limited to educational or assessment purposes.


## K
- K1: remember, recognize, recall
    - at least the `keywords` of each chapter
- K2: understand, explain, give reason, compare, classify, summarize
- K3: apply

## Abbr.
- t : test
- tw : testware

## مدل سوالات
1. فقط یک جواب درست/غلط
2. چند جواب درست/غلط
3. چند جواب درست/غلط، ولی یکی درست ترین/غلط ترین (گزینه های بیشتری رو در بر میگیره)
4. همه/هیچکدام گزینه ها
5. یک گزینه درست که گزینه های درست/غلط دیگر را معرفی میکند


## Chapter 1 : Fundamentals of testing

### Keywords
coverage, debugging, defect, error, failure, quality, quality assurance, root cause, test analysis, test basis,
test case, test completion, test condition, test control, test data, test design, test execution,
test implementation, test monitoring, test object, test objective, test oracle, test planning, test procedure,
test process, test suite, testing, testware, traceability, validation, verification


Complementary tests:
- both primary goal
    - assess work product quality
    - identify defects asap
        - Static Testing: directly
        - Dynamic Testing: evidence / failure
- Static: not running software (type)
    - static analysis on the code (evaluating cmplxity)
    - static analysis on the doc (evaluating readability of use case)
    - review of code or doc
    - locates defects themselves
- Dynamic: running software (level) (Role: testing)
    - locates failure caused by defects

User Acceptance Test:
- Verification: checking against specifications
- Validation: does system meets user's and stakeholders requirement?

Maintanance Testing => Regression testing

Debugging (Role: development)
    - is not testing
    - resolves defect
        - confirmed by confirmation testing (Role: testing)


How **testing is contribution to systems's success**?
- tester involved during review/refinment
- tester works with system designer >> better tests
- tester works with developer
- tester verify and validate before release

**Quality Management**
- Quality Assuarance is a part of it to directing and controlling regarding quality
    - concerns processes
- Quality Control
    - concerns product rather than processes


- Error (mistake)
- Defect (fault / bug)
    - human introduces it to the software
    - humans are affected by distraction/prssure / complex stuff
    - mostly introduces in sys requirment/specif/design
- Failure
    - unexpected behaviour of sys / cmpnnt

Phase Containment
    - ideal: find the defect in the phase of introduction (same lifecyle of development)
    - the cost of removing defect increases as on later life cycles

A **root cause** is generally an organizational issue whereas a cause for a defect is an individual action.


Seven Principals:
1. Testing shows the presence of the defect, but not their absence [not all tests possible]
    - Defect Detection Percentage (DDP)
    - Zeno's Paradox
2. Exhaustive testing is not possible [cant run all possible tests]
    - risk-based testing (prj + prd stakeholders) (focus: level of risk)
        - risk item
        - rate them
        - define tests for items 
    - required-based testing (testers > spec req) (focus: priority)
3. Early testing saves time and money ( shift left ) [start testing early]
    - static + dynamic
    - specially **unit testing**
4. Defects cluster together
    - a small number of modules usually have the most of defects
    - helpful for testers
5. Pesticide Paradox
    - if the same tests are repeated over and over , no longer finds the defects
    - right test strategi -> adequate coverage
6. Testing is context dependant
    - defines how much and how we do testing
7. Absence-of-errors is a fallacy


### 1.4 Test Process

> Test execution is the most visible testing activity

Effective and efficient testing:
    - tests designed and impl to cover good area of software
    - exectution in right seq
    - results reveiewed regularly


the best test process depends on test objectives & can vary company by company
    - SDLC and methodoloigy
    - test level and types
    - prod and prj risk
    - busnes domain
    - op. constraint
    - org. policies and practices
    - req. ext. and int. stds



- **Coverage** (a KPI (Key Performance Indicator))
    - is partial measurement of the thouroughness of testing
    - is percentage of coverage items
    - Levels (at least once):
        - system: every user story 
        - integration: every communication path
        - component: every module/brnach/stmnt
        - env config
        - user persona/stake holder
    - - if traceable, coverage can be measured

- **Test basis** where tests come from



- Test activities and tasks (the various things that testes do)
    1. Test Planning
        - define objectives and approaches
        - how to test sys's confg (if part of sys)
    2. Test monitoring and control
        - monit
            - continuesly compare actual progress agains plan (using monit. metrics)
            - by Exit Criteria (= Definition of Done)
        - ctrl: take ncessary actions
    3. Test analysis (what to test?)
        1. Analyze test basis appropriate to test level
        2. Evaluate test basis and test items to verify diff types of defect may occure (lack/extra/dup/miss)
        3. identify features and sets of them to be tested
        4. Identify and priot test condit
        5. Cpature bi-directional tracebility

        - side-effect: identify what to test -> find defects
        - BTDD / ATTD
    4. Test design (how to test?)
        - more specific (test components)
        - can identify defects
        1. Design and priot
        2. identify test data for test condition
        3. des tst env
        4. capture bi-dir traceblty
    5. Test implementation (everything ready to run the test?)
        - test procedures (t scripts) > **invlv t cases in particlr order**
        - high-lvl to low-lvl t
        1. develope
        2. create **t suites**
        3. arrange in **t execution schedule** >>> efficient t exec
        4. build t env
        5. prep t data
        6. verify bi-dirc
    6. Test execution
        1. rec identities items/object/sys
        2. exec man/auto test
        3. compare res with expecteds >>>> otherwise defect
        4. analyze anomanlis
        5. report defects
        6. log t outcome
        7. rep activity ~regr. t
        8. verify bi-dir
    7. Test completion
        - collect data from completed t activt
        - when?
            - release
            - t prj compl/cncle
            - agile sprint compl
            - t lvl compl
            - mntnce compl
- Test work products (the things produced by and used by testers)
    - any type of info used in testing (+ dev)
    - created as part of t process
    1. Test planning
        - include Entry (= Definition of Ready) & Exit Criteria (= Definition of Done)
        - doesnt contain details
        - must be understandble
        - cover whole prj / t lvl/type
    2. Test monitoring and control
        - regular diff typs of reports
    3. Test Analysis
        - incl t cond which is output of t analysis actvt
    4. Test design
        - resulting t cases + sets of t c
        - may incl t data / env
    5. Test Implementation
        - t procedures
        - t suites
        - t exec schedul
    6. Test Execution (we want to know what happened when test run)
        - status of indiv
        - defect reports
        - doc of which item/obj/tool tested
    7. Test completion (**closure to whole t proces**)
        - t summary rep
        - action for imprv
        - CR / prd bklg
        - finaize tw
- Traceablitly between the test basis and test work prods. and why this is impo
    - ables to measure coverage

| TDD | Focus |
| -- | -- |
| Behaviour-Driven Development (BDD) | behaviour of the sys |
| Acceptance test-driven Development (ATDD) | user view of the sys |

> **Test Oracle** A source to determine an expected result to compare with the actual result of the system under test.


### 1.5 Psychology of Testing


## Chapter 2 : Testing throughout the software development life cycle

### Keywords
acceptance testing, alpha testing, beta testing, change-related testing, commercial off-the-shelf (COTS),
component integration testing, component testing, confirmation testing, contractual acceptance testing,
functional testing, impact analysis, integration testing, maintenance testing, non-functional testing,
operational acceptance testing, regression testing, regulatory acceptance testing, sequential development
model, system integration testing, system testing, test basis, test case, test environment, test level, test
object, test objective, test type, user acceptance testing, white-box testing


### 2.1 SDLC Models
- Sequential Development
    - next phase in only supposed to start when previous one is complete
    - Waterfall:
        - defects are found very late
        - testing added lead time (at the end of prj)
    - V-model
        - testers collab with dev & busns anlst
        - defects are fnd in t basis docs
        - validtn & veriftn
        - 4 t lvls:
            - component
            - integraiton
            - system
            - acceptance
- Iterative / Incremental
    - prj init -> high lvl t planing
    - each iter -> detailed pln / des / t impl
    - issues:
        - more reg t
        - defects outside iter scope
        - less thorough testing
        - danger of less thoruogh testing
        - danger of less formal testing
    - Rational Unified Process (RUP)
        - inception
        - elaboration
        - construction
        - transition
    - Scrum (Agile)
        - cross-functional team
        - 3-9 people
        - sprint : delivery of a unit of work
        - the greates value, soonest
        - ⚠️ good comnctn needed
    - Kanban
        - limit wip & focus
        - focus on end user
    - Spiral (Prototyping)
        - based on risk
        - determin objectives -> identify risk and alternatives -> develope & t -> plan nxt iter

    

#### 2.1.2 SDLC models in context
choose based on:
1. prj goal
2. prj / prd type
3. bsns priot (e.g. time to mrkt)
4. identified prj/prd risks

----> then determines:
    - t lvl can be defined
    - suitable SDLC model

> commercial off-the-shelf (COTS): A type of product developed in an identical format for a large number of customers in the general market.


### 2.2 Test Levels

> Test level: an instance of the test process. groups of test activites that are organized and managed together

Includes:
- specifc t objective (the reason for des and exec that t)
- t basis / wrk prd used to derive t cond / t cases
- t obj (what is tested?)
- typical defects/failures we are looking for at this t lvl
- spcfc approach / rsponsbilt

**each t lvl needs a t env**
- Acc T --> prd env
- Cmpnnt --> dev env
- Sys --> ! external env

#### 2.2.1 Component Testing (= unit / module)
- search for defects in
- verify funclty of
- separately testable

includes:
- Reducing risk
- Verifying whether the functional and non-functional behaviors of the component are as designed
and specified
- Building confidence in the component’s quality
- Finding defects in the component
- Preventing defects from escaping to higher test levels

isolated tests --> mock objs/stubs/drivers are used to simulate

functional / non-functional / perfrmnc / structrual

test basis:
- detailed des
- code
- data model
- cmpnt sepc


Test-first approach = test-driven development (TDD)
- typically in Agile
- highly iterative
- build only what is needed


#### 2.2.2 Integration Testing
tests interfaces between components / sys

Component A integrated with B
- communitcation btwn these 2 compnnt is important 
- not the functionality of each

based on sw & sys des (high + low lvl) & sys arch
- Compnnt Intg:
    - after compnnt testing
    - good candidate for automation
    - in practice may not be done at all
- Sys Intg:
    - btwn diff sys / pkg / ms
    - after sys t
    - in parallel with others
    - may need env




**Objectives**

| Component Testing | Integration Testing |
| ---- | ---- |
| <li>Reducing risk</li><li>Verifying whether the functional and non-functional behaviors of the component are as designed</li>and specified</li><li>Building confidence in the component’s quality</li><li>Finding defects in the component</li><li>Preventing defects from escaping to higher test levels | </li><li>Reducing risk</li><li>Verifying whether the functional and non-functional behaviors of the interfaces are as designed</li>and specified</li><li>Building confidence in the quality of the interfaces</li><li>Finding defects (which may be in the interfaces themselves or within the components or systems)</li><li>Preventing defects from escaping to higher test levels |

**Test basis**

| Component Testing | Integration Testing |
| ---- | ---- |
| <li>Detailed design</li><li>Code</li><li>Data model</li><li>Component specifications | <li>Software and system design</li><li>Sequence diagrams</li><li>Interface and communication protocol specifications</li><li>Use cases</li><li>Architecture at component or system level</li><li>Workflows</li><li>External interface definitions | 


**Integration testing approaches**
1. Big bang integration testing:
    - is a testing approach where all components or modules are integrated and tested as a single unit. This is done after all modules have been completed and before any system-level testing is performed
    - done before intg testing started
    - disadvntg
        - time consuming
        - hard to find defect root-cause
2. Incremental
    - all programs are integrated 1 by 1 and tests are carried out after each step
    - defects+causes are found early
    - disadvntg
        - time consuming to setup mock/stub
    - Possibilities:
        - Top-down
            - GUI
            - compnnt / sys are subsituted by stubs
        - Bottom-up
            - - compnnt / sys are subsituted by drivers
        - Functional incremental

> a risk analysis of the most cmplx interfaces can help to focus integration testing


#### 2.2.3 System Testing
- Bhavr of the whole sys/prd
- high-lvl bhvr
- focus on e2e tasks that sys should perform: non-func => performnc
- sometimes data quality t is impo
- reg suites
- conformance to legal / regulatory req / external stds are tested
- t env should correspond to production env as much as possible
- often the final t / done by specialists (not dev themselves)


#### 2.2.4 Acceptance Testing
- at the end -> sys is ready for release / end user
- defects are not main goal
- FOCUS on VALIDATION
- user + op confidence + confirming compliance to stds

1. User Acceptance Testing (UAT)
    - tests on behalf of real users
    - real/sim env

2. Operational (Production/Factory/Site) Acceptance Testing (OAT)
    - for sys admins
    - keep sys running & recover quickly
    - sec/ins/unins/data

3. Contractual & Regulatory Acceptance Testing (CRAT)
    - sys is in conformance with the contract / regulation
    - tests by users/independant testers

4. Alpha (inside company) & Beta (user's home/office) Testing
    - used for COTS sw
    - early real users to give feedbak / find defects
    - Alpha:
        - users are invited to the company office and tests are done under dev supervision
        - ❌ Field Testing will be performed by the people at client own locations 
    - Beta:
        - user installs on real-world condition/env
        - remotely sends data/feedback to dev company
        - more visible

### 2.3 Test Types
- both done at all lvls
> A **test type** focuses on a particular t objective


#### 2.3.1 Functional (~ ⚠️ black-box / specification) Testing
- **what the sys does**
- typically described in work prd (sometimes undocumented) = specification-based ~= (also can be) experienced-base
- Focus:
    - suitability
    - interoprability
    - security
    - accuracy
    - compliance
- Perspectives:
    - Requirement-based
        - uses specfn of funcl req
        - list of items to test
    - Business-process-based
        - uses knowledge of the busns processes
        - use cases are very helpful
- Measurable: coverage of functional elements


#### 2.3.2 Non-functional Testing (quality characteristics/attributes)
- **how well the sys does what it does**
- Tests:
    - performance
    - load
    - stress
    - usability
    - maintainablity
    - reliabality
    - portability
    - security
- Measurable: coverage of non-functional elements
    - like major group of users

> ISO / ISE / IEC

#### 2.3.3 White-box (structural / glass-box) Testing
- tests internal structure/impl of sys/compnnt
- what is hapening inside the box?
- a way of measuring coverage
- at any t lvl but mostly in cmpnnt t / cmpnnt intg


#### 2.3.4 Change-related Testing
- a change in sw --> a change in it's functionality
- 2 specific test:
    1. Confirmation testing (re-testing)
        - the change itself
    2. Regression testing
        - any other effects of the change (even env)
        - reg t suite/pack
        - good to have 1 suite for all t lvl
            - if suite got very big, eliminate overlapping / low-risk cases
        - candidat for automation
        - Risk analysis helps to decide where to focus

#### 2.3.5 Test Types & Test Levels
good & practical financial example


### 2.4 Maintenance Testing
DONE on an existing operational sys

> Testing the changes to an operational system or the impact of a changed environment to an operational system

> Maintainability: The degree to which a component or system can be modified by the intended maintainer

Factors:
    - degree of risk of change
    - the size of the current sys
    - the size of the change


#### 2.4.1 Triggers for maintenance
- modificaiton
    - SW / HW
    - db / security / planned release / env / ...
- migration
    - siwtch platform
- retirement
    - archiving

#### 2.4.2 Impact Analysis & Regression Testing
makes maintenance testing more efficient

factors that make the impact analysis hard:
- out-dated spec
- not documented t c
- failing bi-dir traceblty
- week tool support
- no knowledge of dev
- not considered maintanblty


## Chapter 3 : Static Techniques

### Keywords
ad hoc review, checklist-based review, dynamic testing, formal review, informal review, inspection,
perspective-based reading, review, role-based review, scenario-based review, static analysis, static
testing, technical review, walkthrough

### 3.1 Static Techniques and the Test Process
- helps finding the defects directly in work products
- efficient way
- find certain defects hard to find in dynamic testing
- everywhere anlsis is crucial before execution (nuclear/medical/sec/)
- generally used before any test execution on the sw

**Static Analysis**
- is a tool-supported form of automated (evaluation) static testing
- apply to review (which is part of static testing , not static anlsis)
- involves use of tools to do the analysis on formal lngs

Mostly evaluate code against various criteria (lint / dead code/variable / never-reached if branch), but Static Testing is a broader eval. review can apply to **any** kind of work product (req / story / web page / doc / budget / ...)

**Static Testing**
Two main advntg:
1. Since can start early in the life cycle, early feedback on quality issues can be stablished
2. Detecting defects ar early stage --> lower costs

- it is a suitable method to improve software work products quality
- good to be used in sprints / iterative methodoligies

work prd are examined **manually = nothing is executed**

all human-readable sw wrk prd can be tested using **review techniq**. defects:
- requirements
- design
- coding (static analsis tools / lint)
- deviations from std
- incorrect interface specifications
- sec vuln
- traceablity problems (covarge)
- maintainbality defects (bad modularizaton / code smells / ...)


> compared to D T , finds defects rather than failures. D T has to investigate failure to find the defect


### 3.2 Review Process
- Formal Review
    - **inspection** = the most documented and formal
    - participation of the team
    - documented results
- Informal Review
    - not documented
    - 2-person team can conduct = pair-working
    - example:
        - walkthrough
        - technical

#### 3.2.1 Review process
- Planning
    - Defining the scope of review -> what to review & quality characteristics to be eval in review
    - estimaing effort  & time
    - identify rev char
    - selec people
    - defining entry & exit criteria
    - check entry is met before review starts
- Initiate review (= kick off)
    - distribute the wrk prd
    - explain scope/obj/roles
    - answer any question
- Individual review (preparation)
    - reviewing all/part of the doc/wrk prd
    - noting potential defec/question/recom
    - Notes:
        - checklist makes it effective & efficient
        - checking rate = number of pages review per hour
            - norm 5-10 p/h
            - in inspection much less
            - should not be exceeded
- Issue communicating and analysis (= review meeting)
    - called *issue* bcz we dont know if defect/not
    - commnct possible defects
    - eval doc
    - reject/accept
    - Communtiocations:
        - Logging
            - indiviual reviewer mention page by page / reviewer by reviewe
            - no real discussion allowed, handled in the dicussion part
            - severity should be defined
                - Critical: defect will cause downstream damage
                - Major: defect will cause downstream effect (bad design --> faulty impl)
                - Minor: defect will not cause downstream damage (non-compliance to stds)
            - 1/2 defect per min
        - Discussion
            - moderator eases the atmosphere
            - outcomes/quality charac are documented
        - Decision-making
            - most impo exit criteria: defect found per page
            - thoroughness of the rev process
- Fixing (= rework) and reporting (= follow up)
    - creating defect report
    - informing the author / team
    - \* it is author's repsonsbility to judge if it is a real issue
    - \* report also ignored issues


#### 3.2.2 Roles and responsibilities
> key success factor: trained/xperineced participants

1. Author
    - create wrk prd
    - fixing that (if needed)
2. Management
    - plan meeting
    - assign resources (people / money)
    - monitor
    - \* in **inception** manager should not be facilitator
3. Facilitator (moderator) (what happens inside the events)
    - ensure effective meeting
    - medaiting btwn povs
    - success depends on him
    - leads meetings
    - checks entry/exit + wrk prd
4. Review leader (organizing the event)
    - takes overall respo for the rev
    - decides who to involve
5. Reviewers (checker / inspector)
    - identify pot defects
    - expert
6. Scribe (recorder)
    - defects found during the meeting

#### 3.2.3 Types of Review
factors:
    - prj
    - availble resources
    - prd type & risks
    - bsns domain
    - company culture

1. Informal Review (buddy check / pairing / pair review) (LEAST FORMAL)
    - main purpose: finding defects
    - possible advntg: gen new ideas/solution
    - checklist : optional
    - very common in Agile dev
    - not documented
    - no rev meeting

2. Walkthrough
    - Main purpose: finding defect / improve / alternative / conformance
    - possible advntg: KT / train / exchng idea
    - scribe : mandatory
    - checklist : optional
    - potential logs
    - led by: author

3. Technical Review
    - Main purpose: gaining consensus (agreement) / pot defects
    - Possible advntg: eval quality / build confidence / new ideas
    - scribe : mandatory
    - checklist : optional
    - indiviual experts (key roles) & prepared before meeting

4. Inspection (MOST FORMAL)
    - Main purpose: find / prevent
    - scribe : mandatory
    - indiv prep is required


#### 3.2.4 Applying Review Techniques
1. Ad hoc reviewing
    - no structured process / instruction / guidance
    - if all use this, it is waste of time
2. Checklist-based Reviewing
    - guided by a list of questions / required attributes
    - good to add checklist of something missing/wen wrong before
    - useful for any type of wrk prd
3. Scenario-based Reviewing and Dry Run (= rehearsal/exercise)
    - the review is guided by the determining the ability of the wrk prd to address specific scenario
    - how sys will be used from a specific (realistic) pov 
    - dont be limited / miss features
4. Role-based Reviewing
    - reviewer eval a wrk prd from pov of a diff stakeholder roles (age/impaired/exp|unexp)
    - Persona
        - a profile = a set of characteristics (job+income+age+...)
        - represents target audience = role
5. Perspective-based Reading
    - eval wrk prd from diff viewpoints
    - was devised for inspection
    - stakeholders perspctv: end-user, marketing, desginer, tester, operation
    - epxensive & effective
    - diff specialties
    - use wrk prd to gen new wrk prd / cover missing parts
    - **most effective** : combines aspects of all techniques (except #1)

#### 3.2.5 Success Factors for Reviews
1. Organization
    - having clear objectives
        - during planning stage to define Exit Criteria / DOD
    - pick the right review type & technique
        - consider type & importance & risk lvl of wrk prd
    - rev materials need to be kept updated
    - limit scope of the rev
        - small chunks
        - early & frequent
    - it takes time
    - management support (not blaming) is critical 
2. People
    - pick the right reviewers
        - diff technique ==> diff skills
    - use testers
        - also beneficial for testers to identify relevant conditions & t cases
    - each participant does its own review work well
    - limit scope of the rev and pick things that really count
    - defects found should be welcomed
    - rev meetings are well managed
    - trust is critical
    - how you communicate is important
    - follow the rules but keep it simple
    - train the participants
    - continuously improve process and tools


## Chapter 4 : Test Techniques (Dynamic Testing)


### Keywords
black-box test technique, boundary value analysis, checklist-based testing, coverage, decision coverage,
decision table testing, error guessing, equivalence partitioning, experience-based test technique,
exploratory testing, state transition testing, statement coverage, test technique, use case testing, whitebox
test technique

### 4.1 Categories of test techniques
The purpose of *test technique* is to identify *test conditions*, *test cases* and *test data*.
    - test conditions are identified during analysis
    - then used to define test cases and test data during test design
    - which are used in test implementation.

#### 4.1.1 Choosing test technique
- Type of component/sys
    - financial: boundry value analysis
- Component/sys complexity
    - simple field
        - equivalence partitioning
        - boundry value
    - screen with many fileds:
        - decision table
        - state transition
        - white-box
- Regulatory stds
- Customer/contractual req
    - statement
    - branch coverage
- Risk lvs and risk types
- Test objcetives
- Available documentation (req spec)
- Tester knowledge & skills
- Available tools
- Time & budget
- SDLC model
    - sequential: formal technique
    - iterative: exploratory
- Expected use of the sw
- Prev exp with using t tchnq on that compnnt/sys
- The types of defects expected in the compnnt/sys


![](img/test-techniques.png)

#### 4.2 Black-box (specification-based / behaviour-based / behavioural) [func + non-func]
- **applicable on all lvls (where a spec exists)**
- tester concentrates on what the sys does, not how 
- based on a model (in/formal) of the sys aspects
- \* test basis: sw req, spec, use case, user stories
- \* coverage: measured by the items in req per t basis and tests applied
- \* test cases shows diff/gap btwn waht req wants and what is impled

**1. Equivalence Partitioning (= partition testing) (EP)**
- test cases are designed to exercise equivalence partitions by using one representative member of each partition
- good all round BBTT (black-box test tecnq)
- any lvl
- good to use at first
- divide into partitions (set of t cond)

**Equivalence Partition** (= equivalence class)
- a portion of the value domain of a data element related to the test object for which all values are expected to be treated the same based on the spec

Example:
- balance in range of 0$ to 100$ has 3% interest rate
- over 100$ up to 1000$ has 5%
- 1000$ and over has 7%

- \* partitions can be applied (defined) for both input and output

- \> input partitions:

| $$invalid^1$$ | 3% | 5% | 7% |
| -- | -- | -- | -- |
| -00.01$ | 0.00 - 100.00 | 100.01 - 999.99 | 1000 - ... |

$$\text{(1) user can insert the value/input but it is supposed to be wrong}$$

- \> output partitions:
    - error
    - calculated rates which should match the input

**Features**
- ALL t lvl
- valid/invalid valuses is in a valid/invalid eqiv. partition & should be accepted/reject by cmpnnt/sys
- partitions can have sub-partitions
    - -100 ... 100
        1. valid & neg
        2. valid & zero
        3. valid & pos
- each value belongs to only **one** partition
- positive partitions can be combined
- negative partitions should not be combined --> masking failures


**2. Boundry Value Analysis (BVA)**
- ALL t lvl
- testing at (t c based on) the boundaries between the partitions
- can extend other wb/bb test
- take min & max from valid & 1st & last (invalid)
- no maximum == open boundary

| invalid | valid | invalid |
| --- | --- | --- |
| 0 | 1 ... 99 | 100 |


**Extending EP & BVA**
- Applying to more than numbers
    - a set of ENUM input which boundary value is nonsense, but invalid value is meaningful
- Applying more than once
    - different values: #,099,100,699,700,99,1234
- Applying to output
- Applying to more than human inputs
- 2 & 3-value boundary analysis
    - in table above:
        - 2-value: 0, 1
        - 3-value: 0, 1 & 2
- \* Good approach to group each set of boundary values in one test. like one test containing all minimum boundaries
- \* Test partitions separately from boundaries. Choose diff partition value than boundaries
    - ==> EP + BVA better than 3-value BVA

**Which EP & BVA?**
- \* experience helps alot

| Approach | Partition Valid | Partition Invalid | Boundary Valid | Boundary Invalid |
| --- | --- | --- | --- | --- |
| Thorough | ✅ | ✅ | ✅ | ✅ |
| User Confidence | ✅ | | | |
| Find Defects ASAP | | | ✅ | ✅ |
| System Handles Bad Inputs | | ✅ | | ✅ |

**Testing Combinations**
- Decision Table Testing
- Pairwise Testing
- Orthogonal arrays


**3. Decision Table (Cause-Effect) Testing**
- focus on bsns logic/rule
- good with **combination** of things (: inputs)
- works well with EP
- How?
    1. identify the suitable compnnt/sys
    2. make the combinations of the inputs
    3. create the result table based on the inputs


$$Coverage=\frac{\text{number of columns that have at least one test case}}{\text{total number of columns}}$$


**4. State Transition (Finite State) Testing**
- focus on bsns logic/rule
- can be as detailed / abstract as you need
- Examples:
    - banks account withdrawal > balance status > sufficient / insufficient
    - word processor > document status > open/closed

**State Graph (Chart)**

**Four Elements**
1. The states that the sw may occupy
2. The transition from one state to the othe one (not all transitions are allowed)
3. The events that cause a transition
4. The actions that result from a transition (error msg / expected res)

> 1 event can cause only 1 action

> the same event from another state can cause a diff action & a diff end

> transisitons dont need necessarily to change to a diff state

**X-switch:**
- 0-switch: coverage of all transitions
- 1-switch: coverage of transition pairs
- 2-switch: coverage of transition triples

**State Table**
- good for indicating negative states


**5. Use Case Testing**
- helps us identify test cases that exercise the whole system on a tx by tx basis from start to finish
- Tests can be derived from use cases, which are a specific way of designing interactions with software
items. 
- They incorporate requirements for the software functions
- Use cases are associated with actors (human users, external hardware, or other components or systems) and subjects (the component or system to which the use case is applied).
- UCs are defined in terms of the actor, not the sys = what actor does/sees
- uncover integration defects
- finds well real-world defects
- must specify pre/postconditions to be met/expected



#### 4.3 White-box (glass-box / structure-based / structural)
- ISO/IEC/IEEE 29119-4
- **applicable on all lvls**
- uses internal structure
- \* test basis: code, sw arch, detailed des, src of info regrding sw structure
- \* purpose:
    - coverage measurement
    - structural test case design
- \* coverage: items tested within a selected structure
- \* determine the path -> specific input -> specific output <- **oracle** to match

**Levels:**
- Component (focus on structure)
    - statement
    - decision
    - branches
    - distinct paths
- Integration
    - examine how modules call each other = Call Tree
- System
    - menu structure
    - bsns process
    - webpage structure

**Coverage**
- The degree to which specified coverage items have been determined or have been exercised by a test suite expressed as a percentage.
- applied to both WB & BB techniques
- Product Owners
    - target: percentage of req that have been tested
    - tool: req/tst mngmnet tool
- Programmer:
    - target: code


$$Coverage=\frac{\text{number of coverage items[1] exercised}}{\text{total number of coverage items}} * 100\%$$


$$\text{1. Anything that can be tested and countable}$$

**Pitfalls of coverage**
1. 100% t cvrg doesnt mean 100% tested
2. two diff test may achieve the same cvrg but with diff input and diff error finidng
3. Coverage (in WB) looks at only what is there (exist), not on not-implemented. but BB can find what doesnt exists (but needed in spec)
4. cvrg doesnt say anything about the sys quality

> Coverage is one way of assessing what one aspect of thoroughness & depends on what is measured. Is best done by using tools

**1. Statement (Line of Code) Testing & Coverage**
- Goal: the least tst to go through all lines of code

$$\text{Statement coverage}=\frac{\text{number of statements exercised}}{\text{total number of statements}} * 100\%$$

Example:

```
1. Read A
2. Read B
3. C = A + 2*B
4. IF(C > 50) THEN
5.      PRINT 'BIG C'
6. ENDIF 
```

| Test Case | Statement Coverage |
| --- | --- |
| A = 2, B = 10 | 80% |
| A = 1, B = 25 | 100% |

**2. Decision Testing & Coverage**
- Goal: check every possible decision (Tru & False)
- wherever there are 2 or more possible outcomes
    - If
    - Loop control (do-while / repeat-until)
    - case

$$\text{Decision Statement coverage}=\frac{\text{number of decision outcomes exercised}}{\text{total number of decision outcomes}} * 100\%$$

> **Decision coverage is stronger than statement coverage** --> 100% DC guarantees 100% SC

| Test Case | Decision Branch |
| --- | --- |
| A = 2, B = 10 | FALSE |
| A = 1, B = 25 | TRUE |
| Total Coverage | 100% |

#### 4.4 Experience-based
- people's knwoledge/exp/skills contributes mainly to the t condition/case/data
- exp of both technical & busns people is impo --> for t analsis & design
- both behavioural & structural insights are used to des exp-based tests
- less systematic (**non-systematic**) but may be more effective
- used for low-risk sys & under extreme time prssure
- difficult -> measurement of coverage


**1. Error Guessing**
- complement to the other formal techniques
- very much dependant on teh skill of the tester
- no rules, think of situations sw may not cope
- structured way: list possible defects
- **Attack / Fault Attack:** forced specific type of failures


**2. Exploratory (session-based) Testing**
- **under time pressure**
- minimum planning, maximum test execution
- Planning:
    - creation of test charter (often written in advance)
    - a short desc of the scope of a short (1-2 hour) time-boxed tst effort
    - objectives and possible approaches
- Test des and exec in parallel
- informally = no doc
- done in sessions
    - max 90 min
    - tst charter gives the list (objectives)
    - dedicated to testing, nothing more
- Test logging
    - durinig exec
    - documented at high lvl
- key aspect is Learning


**Checklits-based Testing**
- based on exp but those are summarized and doc as checklists
- checklist items are used to des, impl & exec tsts
- checklists can be modified/improved
- can be general/specific (aimed)
- diff ppl may find diff defects


**McCabe’s Cyclomatic Complexity**

is a software metric that is used to measure the complexity of a software system by analyzing its control flow graph. It was introduced by Thomas McCabe in 1976 as a way to quantify the number of independent paths through a program's source code.

Cyclomatic Complexity is calculated based on the number of decision points, such as conditional statements and loops, in the source code. The formula for calculating Cyclomatic Complexity is:

$$M = E - N + 2P$$

    M = Cyclomatic Complexity
    E = the number of edges in the control flow graph
    N = the number of nodes in the control flow graph
    P = the number of connected components in the control flow graph

The resulting value of Cyclomatic Complexity can be used to help identify areas of the code that may be more difficult to test or maintain. Higher values of Cyclomatic Complexity indicate more complex code with more potential paths and therefore may require more thorough testing and may be more prone to errors.

Cyclomatic Complexity is one of several metrics that can be used to evaluate software quality and maintainability. It is widely used in software development and testing, and is supported by many software development tools and integrated development environments (IDEs).


## Chapter 5 : Test Management


### Keywords
configuration management, defect management, defect report, entry criteria, exit criteria, product risk,
project risk, risk, risk level, risk-based testing, test approach, test control, test estimation, test manager,
test monitoring, test plan, test planning, test progress report, test strategy, test summary report, tester

### 5.1 Test Organization

#### 5.1.1 Independent Testing
- No independent testers; the only form of testing available is developers testing their own code
- Independent developers or testers within the development teams or the project team; this could be developers testing their colleagues’ products
- Independent test team or group within the organization, reporting to project management or executive management
- Independent testers from the business organization or user community, or with specializations in specific test types such as usability, security, performance, regulatory/compliance, or portability
- Independent testers external to the organization, either working on-site (in-house) or off-site (outsourcing)


**Benefits & Drawbacks**

**Influences**
- As the size, complexity and criticality of the prj increases, it is impo to have independence in later levels of testing (intg, sys, acptnc)
- diff tstng lvls -> diff ind -> higher lvls -> more ind
- SDLC
    - : Agile: prd owner may do accptnce tstng at end of sprint

#### 5.1.2 Tasks of a Test Manager and Tester
Depends on:
    - organization
    - prj & prd context
    - skills of the individuals

**Test Manager**
- overall resp for success / manage the testing
- skilled / senior
- hierarchy:
    - test coordinator / test coach
        - test leader / lead tester

**Tester**
- review and contribute to the plan
- automate test
- setup tst env

### 5.2 Test Planning & Estimation
Plans, estimates, strategies --> depend on : lvl, objevtives, targets

**Test Plan:** documentation describing the test objectives to be achieved and the means and the schedule for achieving them, organized to coordinate testing activities
    - it is not detailed like tst des, tst case, tst procedure
    - is an ongoing activity througout the SDLC (and even into maintenance)
    - can depend on HW/SW --> diff tst plans -> to remove redundancy, also have a master plan

1. to guide our thinking
    - using a template
2. to communicate to others
    - keeps the commumnication of team
3. to help to manage future changes

> Diff lvls can have diff plans to be run in diff time period for diff objectives

During tst analysis and des, you may need to reduce gaps and overlapping btwn tst lvls. it is usually odne in Master Test Plan

coordinating btwin tst lvls & coordinating tst works

#### 5.2.2 Test Strategy & Test Approach
Test Strategy: Documentation that expresses the generic requirements for testing one or more projects run within an organization, providing details on how testing is to be performed and is aligned with the test policy

Test Approach: the implementation of test strategy for a specific project. So define & document it in test plans, refininf & providing furthur details in the test design.
    - powerful factor on successful test effort & accuracy of test plans

**Major types:**
- Analytical
    - tests are determined by some factors, like: documents / test basis / risk
    1. Risk-based Strategy
    2. Requirement-based Strategy
    - 1 & 2 may use in/formal alanytical technique during req/des stages of the proj
- Model-based
    - tests are based on some model of the test object
    - models like:
        - bsns process models
        - state models (state transition diagrams)
        - reliabilty grown models
- Methodical
    - a predefined and fairly stable list of test conditions (checklist..) is used
    - industry standard for SW quality = ISO/IEC 25010
- Process-compliant / Standard-compliant
    - an external standard or set of rules is used to analyze, design and impl tests
    - often with little (if any) customization
    - early or late point of involvement
    - ISO / IEC / IEEE 29119-3
- Directive / Consultative
    - stakeholders or experts may direct the testing according to their advice/guidance
    - experts:
        - technology / bsns domain experts
        - users
        - developers
    - *Consultative*
        - a group of non-testers
        - outsourced
        - usually at the end stages of SDLC
- Regression-averse
    - sys's performance is not deteriorated after change/enhancement
    - regression tests/suites are used (usually automated)
- Reactive (dynamic) (= exploratory)
    - test react and evolve based on what is found during execution, rather than being designed/impl before exec
    - find defect as much as possible and expand the test
    - typically late stages of testing
    - attack-based / exploratory approach

| Preventive (early, cheap) | Dynamic (late stages, sys is ready) |
| -- | -- |
| Analytical | Reactive |


**How to choose the best strategy?**
- Risks
    - risk management => risks & lvls
    - example:
        - well-stablished  & slowly growing prj => *Risk = regression ==> Regression-averse*
        - new application => *diff risks ==> Risk-based Analytical*
- Skills
    - do u have the skills to execute that strategy? if not, pick *Standard-compliant* rather than creating yours
- Objectives
    - satisfy the needs
    - e.g. u need to find defects as many as possible? ==> *dynamic/reactive*
- Regulations
    - to satisfy regulators and stakeholders
    - e.g. meet all requirements ==> *Methodical*
- Product
    - prj/sys has well-specified requirement ==> *Requirement-based Analytical*
- Business
    - when bsns considerations & bsns continuity are impo
    - if u can use a legacy sys as model for new system ==> *Model-based*

#### 5.2.3 Entry Criteria (definition of ready) & Exit Criteria (definition of done)
1. Entry Criteria (definition of ready)
    - the set of conditions to officially start a defined task
    - Availability of:
        - tst basis
        - tst items from prev. lvl
        - tst env
        - tst data/resrouces
        - tst tools
        - tst staff
        - tst cmpnnt/sys/SW/HW
2. Exit Criteria (completion criteria / test completion criteria / defintion of done)
    - the set of conditions to officially complete a defined task
    - Factors:
        - tests
        - coverage
        - defects
        - quality (non/func)
        - money (cost of finding in this lvl compared to next)
        - schedule
        - risk (e.g. too early == not tested / too late == losing market share)
    
#### 5.2.4 Test Execution Schedule
Schedule execution of tests in a test suite:
- priority of tst
- tech/logical dependancy
- type of tst (reg / confirmation)

#### 5.2.5 Factors influencing the test effort
**Estimating what the test involves and what it will cost ** *even if input data is incomplete/uncertain*
- **Work** 
    - *Forward:* start with planning and move fwd step-by-step
    - *Backward:* consider the risks identified during risk analysis

- Performance test env aquisition and configuration is an activity in the test impl activity
        - has a detailed test plan

**Factors that affect the test effort**
- Major inf: test strategy & approach
1. Product
    - risks
    - quality of test basis
    - regulations
    - size
    - requirements
2. Development Process (how test effort is spent)
    - the stability & maturity of organization (the more, the more saved)
    - TDLC
        - V-model = more fragile in late changes
        - Agile = high regression testing cost
    - test approach
    - test tools (dev & debug -> test completion)
    - test process. the more mature, the more efficient & effective
    - time pressure
3. People (execute the process)
    - skills & experience. domain knowledge
    - team cohesion and leadership
4. Test Results
    - the number and severity of defects found
    - the amount of rework required


#### 5.2.6 Test Estimation Techniques
1. Expert-based (bottom-up)
    - consulting the people involved & have experience
    - it starts at the lowest lvl of the hierchical breakdown in the work-breakdown structure (the task) and let the duration, effort, dependencies and resources for each task add up across all the tasks
    - : Agile > Planning poker
    - : Sequential > Wideband Delphi estimation
2. Metrics-based
    - analyzing metrics from past projects and from industry data
    - : Burndown charts
    - : Defect Removal models
  
### 5.3 Test Monitoring & Control (of impl & exec)
- Test Monitoring (activity)
  - *a test management activity* that involves checking the status of testing activities, identifying any variances from the planned or expected status & reporting status to stakeholders
- Test Control (task)
  - *a test management task* that deals with developing and applying a set of corrective actions to get a test project on track when monitoring shows a deviation from what was planned


#### 5.3.1 Metrics used in testing
Purpose of test progress monitoring info:
- Progress against the planned schedule and budget
- Current quality of the test object
- Adequacy of the test approach
- Effectiveness of the test activities with respect to the objectives

*Measuring test progress based on defects found and fixed is common*

Common metrics for test progress monitoring:
- Percentage of planned work done in test case preparation (or percentage of planned test cases
implemented)
- Percentage of planned work done in test environment preparation
- Test case execution (e.g., number of test cases run/not run, test cases passed/failed, and/or test
conditions passed/failed)
- Defect information (e.g., defect density, defects found and fixed, failure rate, and confirmation test
results)
- Test coverage of requirements, user stories, acceptance criteria, risks, or code
- Task completion, resource allocation and usage, and effort
- Cost of testing, including the cost compared to the benefit of finding the next defect or the cost
compared to the benefit of running the next test

#### 5.3.2 Purposes, Contents, and Audiences for Test Reports
**Content:**
1. Test Progress Report (test status report)
    - at regular intervals throughout the project
    - result in test control actions
2. Test Summary Report (test report)
    - test items against exit criteria
    - final test progress report for the whole prject
    - at the end of test activity/lvl

**Audience**
- ISO/IEC/IEEE 291119-3
- CEO
    - concise
    - summary of defects 
    - percentage passed
    - budget & schedule
- Dev
    - detailed defect types & trends

#### 5.4 Configuration Management
- A discipline applying technical and administrative direction and surveillance to identify and document the functional and physical characteristics of a configuration item, control changes to those characteristics, record and report change processing and implementation status, and verify that it complies with specified requirements.
- Determining clearly what the items are (code, sw, hw, test, ...) that make up the sw/sys
- manage them carefully
- version controll everything
- decide about procedures and tools during project/test planning stage

#### 5.5 Risks & Testing
**Risk**
    - a factor that could result in future negative consequences

1. Project Risk
    - impacts project success
    - direct risks:
        - late delivery of test items
        - availability issue of test env
    - indirect risks
        - excessive time repairing defects
        - getting professional sys admin for test  env
2. Product Risk (= quality risk)
    - impacts the product quality
    - sys/sw may fail (non/func : UI / performance)

> documentation is not complete