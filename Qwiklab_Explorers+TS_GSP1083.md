

# AlloyDB - Database Fundamentals || [GSP1083](https://www.cloudskillsboost.google/focuses/50122?parent=catalog) ||

# # Like, comment, share & Don't forget to subscribe [Qwiklab_Explorers_ts](https://youtube.com/@titashshil?si=RgamNu1dc9jVIbJN) 👍😄🤝

---

- **Run the following Commands in Cloud Shell** 

```bash
export REGION=
```

```bash
gcloud beta alloydb clusters create lab-cluster \
    --password=Change3Me \
    --network=peering-network \
    --region=$REGION \
    --project=$DEVSHELL_PROJECT_ID

gcloud beta alloydb instances create lab-instance \
    --instance-type=PRIMARY \
    --cpu-count=2 \
    --region=$REGION  \
    --cluster=lab-cluster \
    --project=$DEVSHELL_PROJECT_ID
```
---

- **Launch Another Cloud Shell +**  

```bash
export REGION=
```

```bash
gcloud beta alloydb clusters create gcloud-lab-cluster \
    --password=Change3Me \
    --network=peering-network \
    --region=$REGION \
    --project=$DEVSHELL_PROJECT_ID

gcloud beta alloydb instances create gcloud-lab-instance\
    --instance-type=PRIMARY \
    --cpu-count=2 \
    --region=$REGION  \
    --cluster=gcloud-lab-cluster \
    --project=$DEVSHELL_PROJECT_ID
```

----

### 🔗 [``VM Instance``](https://console.cloud.google.com/compute/instances?referrer=search&project=)

### 🔗 [``AlloyDB``](https://console.cloud.google.com/alloydb/clusters?referrer=search&project=)


Run the following commands in `SSH` window 

```bash
export ALLOYDB=
```

```bash
echo $ALLOYDB  > alloydbip.txt 
```

```bash
psql -h $ALLOYDB -U postgres
```

---
- **user's password**
```
Change3Me
```
---

```bash
\c postgres
```

```bash
CREATE TABLE regions (
    region_id bigint NOT NULL,
    region_name varchar(25)
) ;

ALTER TABLE regions ADD PRIMARY KEY (region_id);
```

```bash
INSERT INTO regions VALUES ( 1, 'Europe' );

INSERT INTO regions VALUES ( 2, 'Americas' );

INSERT INTO regions VALUES ( 3, 'Asia' );

INSERT INTO regions VALUES ( 4, 'Middle East and Africa' );
```

```bash
SELECT region_id, region_name from regions;
```

---



# Congratulations ..!!🎉  You completed the lab shortly..😃💯

# *Well done..!* 👏

# Thank you for visiting.... :) 🗯️

# [Qwiklab_Explorers_ts](https://youtube.com/@titashshil?si=RgamNu1dc9jVIbJN)
