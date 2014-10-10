```
Query Where
Order	Column
[Customer(ind_customer)::Do Not Contact by Email] Is Not 
[Checked]


(--------------------
    [Customer(ind_customer)::Title] Contains [digital]
    ----- OR ---------------
    [Customer(ind_customer)::Title] Contains [chief]
    ----- OR ---------------
    [Customer(ind_customer)::Title] Contains [Creative]
    ----- OR ---------------
    [Customer(ind_customer)::Title] Contains [technolog]
    ----- OR ---------------
    [Customer(ind_customer)::Title] Contains [innovation]
    ----- OR ---------------
    [Customer(ind_customer)::Title] Contains [emerging]
    ----- OR ---------------
    [Customer(ind_customer)::Title] Contains [lab]
    ----- OR ---------------
    [Customer(ind_customer)::Title] Contains [CTO]
    ----- OR ---------------
    [Customer(ind_customer)::Title] Contains [CIO]
    ----- OR ---------------
    [Customer(ind_customer)::Title] Contains [CXO]
    ----- OR ---------------
    [Customer(ind_customer)::Title] Contains [Experience]
)--------------------
```


```

Query Where
Order	Column
[Customer(ind_customer)::Primary E-Mail] Is Not Null 
[Customer(ind_customer)::Delete Flag] Is Not [Checked]
(--------------------
    (--------------------
        [Customer(ind_customer)::Title] Contains [digital]
        ----- OR ---------------
        [Customer(ind_customer)::Title] Contains [chief]
        ----- OR ---------------
        [Customer(ind_customer)::Title] Contains [Strateg]
        ----- OR ---------------
        [Customer(ind_customer)::Title] Contains [Creative]
        ----- OR ---------------
        [Customer(ind_customer)::Title] Contains [technolog]
        ----- OR ---------------
        [Customer(ind_customer)::Title] Contains [innovation]
        ----- OR ---------------
        [Customer(ind_customer)::Title] Contains [emerging]
        ----- OR ---------------
        [Customer(ind_customer)::Title] Contains [lab]
        ----- OR ---------------
        [Customer(ind_customer)::Title] Contains [production]
        ----- OR ---------------
        [Customer(ind_customer)::Title] Contains [delivery]
        ----- OR ---------------
        [Customer(ind_customer)::Title] Contains [CTO]
        ----- OR ---------------
        [Customer(ind_customer)::Title] Contains [CIO]
        ----- OR ---------------
        [Customer(ind_customer)::Title] Contains [CXO]
        ----- OR ---------------
        [Customer(ind_customer)::Title] Contains [Experience]
    )--------------------
    ----- OR ---------------
    [Customer(ind_customer)::Customer Key] Is In [SELECT reg_cst_key FROM 
ev_registrant  (NOLOCK)  WHE ...
)--------------------

```


```
Query Where
Order	Column
[Customer(ind_customer)::Title] Does Not Contain [assoc]
[Customer(ind_customer)::Title] Does Not Contain [assistant]
(--------------------
    [Customer(ind_customer)::Title] Contains [Chief]
    ----- OR ---------------
    [Customer(ind_customer)::Title] Contains [Digital]
    ----- OR ---------------
    [Customer(ind_customer)::Title] Contains [technolog]
    ----- OR ---------------
    [Customer(ind_customer)::Title] Contains [experien]
    ----- OR ---------------
    [Customer(ind_customer)::Title] Contains [innovat]
    ----- OR ---------------
    [Customer(ind_customer)::Title] Contains [CTO]
    ----- OR ---------------
    [Customer(ind_customer)::Title] Contains [CIO]
    ----- OR ---------------
    [Customer(ind_customer)::Title] Contains [communication]
    ----- OR ---------------
    [Customer(ind_customer)::Title] Contains [relations]
    ----- OR ---------------
)--------------------
----- OR ---------------
(--------------------
    [Event Registrant::Event] Is Equal To [4A's CreateTech 2012]
    ----- OR ---------------
    [Event Registrant::Event] Is Equal To [2011 4A's CreateTech]
    ----- OR ---------------
    [Event Registrant::Event] Is Equal To [4A's CreateTech 2013]
)--------------------
----- OR ---------------
(--------------------
    [Affiliation(AllAffiliations)::Role] Is Equal To [AAAA Co-Main Contact]
    ----- OR ---------------
    [Affiliation(AllAffiliations)::Role] Is Equal To [AAAA Main Contact]
    ----- OR ---------------
    [Affiliation(AllAffiliations)::Role] Is Equal To [Account Planning Head] (Ask At Run-Time)
    ----- OR ---------------
    [Affiliation(AllAffiliations)::Role] Is Equal To [Communications Mgr.]
    ----- OR ---------------
    [Affiliation(AllAffiliations)::Role] Is Equal To [Main contact - SFNA Subscriber] (Ask At Run-Time)
    ----- OR ---------------
    [Affiliation(AllAffiliations)::Role] Is Equal To [Main Contact Prospect] (Ask At Run-Time)
    ----- OR ---------------
    [Affiliation(AllAffiliations)::Role] Is Equal To [Public Rel. Contact  (Agency Corp. Comms.)] (Ask A ...
)--------------------
(--------------------
    [Email(email)::E-Mail Address] Contains [@]
    [Email(email)::Invalid E-mail Address] Is Not [Checked]
    [Customer(ind_customer)::Do Not Contact by Email] Is Not [Checked]
    [Email(email)::E-Mail Address] Is Not Equal To [bogus@aaaa.org]
)--------------------

```