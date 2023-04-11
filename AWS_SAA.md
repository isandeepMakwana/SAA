**AWS Accounts**

+-----------+----------------------------------------------------------+
| >         | > **has full access in the AWS account**                 |
|  **ROOT** |                                                          |
+===========+==========================================================+
|           |                                                          |
+-----------+----------------------------------------------------------+
| > **IAM** | > **has no access at all initially**                     |
+-----------+----------------------------------------------------------+
|           | > **access needs to be granted by the root user**        |
+-----------+----------------------------------------------------------+
|           |                                                          |
+-----------+----------------------------------------------------------+

![](media/image3.jpeg){width="7.625in" height="4.072916666666667in"}

+-----------------------+-------------------------------------+--------+
| > *                   | > dora.theodora89+AWS1@gmail.com    | > MDLT |
| *Management/General** |                                     |        |
+=======================+=====================================+========+
|                       |                                     |        |
+-----------------------+-------------------------------------+--------+
| > **Production**      | > dora.theodora89+AWS1@gmail.com    | > MDLT |
+-----------------------+-------------------------------------+--------+
|                       |                                     |        |
+-----------------------+-------------------------------------+--------+

> IAM identities start with **no permissions** on an AWS Account, but
> can be granted permissions (almost) up to those held by the Account
> Root User.
>
> IAM also is trusted full by the account

**What is cloud computing ?**

1.  **On demand self-service:** Cloud can provision capabilities as
    needed **without requiring human interaction.**

-   virtual machines, storage databases, networking

-   using a web page, terminate to access those

-   no delay

2.  **Broad network access:** Capabilities are available over the
    **network** and accessed through **standard mechanisms.**

-   HTTP, HTTPS, SSH, Remote Desktop, VPN

3.  **Resource pooling**:

-   There is sense **of location independence**... no control or
    knowledge over the exact location of the resources

-   Resources are **pooled** to serve multiple consumers using **a
    multi-tenant model**

-   pooling: isolates the customer: your data is only visible for you.

4.  **Rapid Elasticity:**

> Capabilities can be **elastically provisions and** released to
> **scale** rapidly outward and inward with the demand
>
> To the consumer, the capabilities available for provisioning often
> **appear unlimited**.

5.  **Measured Service:** Resource usage can be **monitored, controlled,
    reported** and **billed**.

> on demand billing ![](media/image4.png){width="6.5in"
> height="3.343132108486439in"}

**Public & Private & Hybrid & Multi Cloud**

> **Public Cloud**

-   classify as a cloud

-   available to the general public

> **Multiple-Cloud**

-   one app using multiple clouds (AWS, Azure, Google, etc)

-   if a vendor fails, part of the system can still work

-   multiple clouds can be used a **one** single environment

    -   but in this situation they rely on the lowest common feature set

    -   loosing what makes each vendor unique

> **Private Cloud**

-   meets all 5 characteristics of the cloud

> **Hybrid Cloud**

-   using **private** cloud in **conjuncture** with **public** cloud

-   private cloud and public cloud working in a single environment

-   using same tooling, interfaces and process to interact with both

> **Hybrid environment**

-   using public cloud with a traditional infrastructure

![](media/image5.jpeg){width="6.515955818022747in"
height="3.914773622047244in"}

**Cloud service modules**

> **Infrastructure stack** Some parts are managed by **you**, some are
> managed by the vendor.

![](media/image6.jpeg){width="1.8465277777777778in"
height="3.2291666666666665in"}

> Unit of consumption - what you need to pay that you had consumed.
>
> \- part that are you are responsible to manage
>
> In a \"on-premises\" server (business owns this server)

-   the business needs to own/buy each part of the infrastructure

-   the business needs to manage all parts of the infrastructure

> In \"DC Hosted\"

-   the vendor paid an managed the building, the power, air condition
    > and staff

> Infrastructure as a service **(IAAS)**
>
> With IAAS you pay per second/minute/hour for the virtual machine -
> when you use the virtual machine.

-   the client ignores the building, maintain the infrastructure,
    > hardware, and staff costs

-   EC2

![](media/image7.jpeg){width="5.1409722222222225in"
height="2.9520833333333334in"}

> Platform as a service (**PAAS**)
>
> With PAAS is aimed for developers who have an application and only
> want to run it, without worrying about any of the infrastructure.

-   the apps is put in the runtime environment

-   the vendor manages the containers, OS, virtualization, servers, etc

![](media/image8.png){width="6.863888888888889in"
height="10.002083333333333in"}

> Software as a service (**SAAS**)
>
> In this case you consume the application. The application is what you
> get a service. (Email, Netflix, Dropbox, OneDrive, office, etc)

-   there is no much control how the app works

![](media/image9.jpeg){width="7.420833333333333in"
height="3.4791666666666665in"}

**Public vs Private Services**

> **Public** and **private** keywords in AWS services are referring to
> networking **only**!
>
> When connecting to AWS:

1.  Connectivity is required?

2.  Permissions granted for the user?

> **AWS** is a **public cloud**, it can be connected over the public
> internet.
>
> AWS has a zone called the AWS public zone, which is where public
> services run from, and is connected, and can be accessed from the
> public internet.
>
> The private zone is isolated by default, from the AWS public zone, and
> from the public internet. But these private zones can be configured to
> be public, meaning that part of them, is projected into the public
> zone and then accessed by a public zone.
>
> By default private services can be accessed only from the same private
> networks or any on-premises networks connected to them.

![](media/image10.jpeg){width="7.309027777777778in"
height="3.4541666666666666in"}

![](media/image11.png){width="7.055555555555555in"
height="3.9688910761154856in"}

> **AWS public service is located in the AWS Public Zone and anyone can
> connect but permissions are required to access the service.**
>
> **AWS private service is located in a VPC, accessible from the VPC is
> located in and accessible from other VPCs or on-premises networks as
> long as private networking is configured.**

**AWS global infrastructure**

+-------------------------------------------------+--------------------+
| Thursday, June 10, 2021                         | > 3:53 PM          |
+=================================================+====================+
+-------------------------------------------------+--------------------+

> **AWS** is a global cloud platform, which is a collection of smaller
> groupings of infrastructure connected together by a global high speed
> network.
>
> A **region** in AWS context, is an area of the world they had selected
> that encapsulates a full deployment of AWS infrastructure:

-   compute services

-   database products

-   storage

-   AI

-   analytics

-   etc

> **Edge locations** are smaller than regions, and generally they only
> have content distribution services, and some types of edge computing.
>
> The edge locations are placed in many more places than regions.
>
> Usually, the further the services are from the clients, the slower the
> transfer is, and higher the latency.
>
> Usually regions and edge location are used together by solutions
> architects.
>
> **Regions** are 100% isolated from each other, meaning that if a
> disaster happens in one, the others won\'t be affected.
>
> Regions have geopolitics and governance separation - the client is
> affected by the laws and regulations of the of the region of where the
> infrastructure is located.
>
> Data saved in one region, won\'t leave that region unless configured
> otherwise.
>
> **Regions** give location control, which allows the tunning of
> infrastructure and architecture.

![](media/image12.jpeg){width="7.314583333333333in" height="3.8625in"}

> **Resilience:**
>
> AWS Developer Page 10

1.  **Globally** means that a service operates globally as a single
    > product, and its data is replicated across multiple regions. This
    > means that if a region fails, the services continue to run. (IAM
    > and Route53 are global).

2.  **Region** - this are services that operate within a single region,
    > with one set of data per region. They replicate data in multiple
    > **availability zone** within that region.

3.  **AZ** -they run from a single availability zone.

AWS Developer Page 11

**YAML**

![](media/image13.jpeg){width="4.182638888888889in"
height="2.2104166666666667in"}

> **YAML** is one of the languages, that Cloud uses as a template.

-   human readable

-   define data

-   configuration

-   Key: Value pair

-   supports:

    -   strings

    -   integers

    -   floats

    -   booleans

    -   nulls

    -   Lists cats : \[\"a\",\"b\",\"c\"\] or cats:

        -   \"a\"

        -   \"b\"

        -   \"c\"

    -   ![](media/image14.png){width="7.25839457567804in"
        > height="6.045160761154856in"}dictionary

        -   turtle:

            -   name: \"Pixel\"

> color: \[\"green\", \"grey\"\]

-   name: \"Sid\"

> color: \[\"black\", \"green\"\]

-   **indentation matters**

**JSON**

> JavaScript Object Notation (JSON) - used broadly

-   used for data-interchange format

-   easy for humans to read and write

-   easy for machines to parse and generate

-   does not care about indentation - has brackets

> JSON **object** is an unordered set of **key: value** pairs enclosed
> by curly brackets {} - dictionary
>
> JSON **array** is an ordered collection of values, separated by commas
> and enclosed in square brackets \[\] - list
>
> Values can be:

-   string

-   object

-   integers

-   array

-   Booleans

-   null

![](media/image15.jpeg){width="6.834268372703412in"
height="3.651613079615048in"}

![](media/image16.png){width="6.891666666666667in"
height="10.002083333333333in"}

**Encryption**

+---+---+-----------+---+---------+-----------+-------------------------------+---+
|   |   | **E       |   |         |           |                               |   |
|   |   | ncryption |   |         |           |                               |   |
|   |   | App       |   |         |           |                               |   |
|   |   | roaches** |   |         |           |                               |   |
+---+---+-----------+---+---------+-----------+-------------------------------+---+
|   |   |           |   |         |           |                               |   |
+---+---+-----------+---+---------+-----------+-------------------------------+---+
|   |   | **E       |   |         |           | > **Encryption in transit**   |   |
|   |   | ncryption |   |         |           |                               |   |
|   |   | at rest** |   |         |           |                               |   |
+---+---+-----------+---+---------+-----------+-------------------------------+---+
|   |   | •         |   |         |           | > • Aims to protect data as   |   |
|   |   | Designed  |   |         |           | > is in transit between two   |   |
|   |   | to        |   |         |           |                               |   |
|   |   | protect   |   |         |           |                               |   |
|   |   | against   |   |         |           |                               |   |
|   |   | theft     |   |         |           |                               |   |
+---+---+-----------+---+---------+-----------+-------------------------------+---+
|   |   | •         |   |         |           | > places                      |   |
|   |   | Encrypts  |   |         |           |                               |   |
|   |   | all the   |   |         |           |                               |   |
|   |   | data      |   |         |           |                               |   |
|   |   | written   |   |         |           |                               |   |
|   |   | to the    |   |         |           |                               |   |
|   |   | storage   |   |         |           |                               |   |
+---+---+-----------+---+---------+-----------+-------------------------------+---+
|   |   | •         |   |         |           | > • The data is encrypted on  |   |
|   |   | Decrypts  |   |         |           | > the \"way\" and decrypted   |   |
|   |   | the data  |   |         |           |                               |   |
|   |   | as is     |   |         |           |                               |   |
|   |   | read from |   |         |           |                               |   |
|   |   | the       |   |         |           |                               |   |
|   |   | storage   |   |         |           |                               |   |
+---+---+-----------+---+---------+-----------+-------------------------------+---+
|   |   | • Is      |   |         |           | > when it arrives to the      |   |
|   |   | usually   |   |         |           | > destination                 |   |
|   |   | used if   |   |         |           |                               |   |
|   |   | only one  |   |         |           |                               |   |
|   |   | entity    |   |         |           |                               |   |
|   |   | involved  |   |         |           |                               |   |
+---+---+-----------+---+---------+-----------+-------------------------------+---+
|   |   | > • who   |   |         |           | > • Is usually used when      |   |
|   |   | > know    |   |         |           | > multiple entities are       |   |
|   |   | > the     |   |         |           | > involves                    |   |
|   |   | > e       |   |         |           |                               |   |
|   |   | ncryption |   |         |           |                               |   |
|   |   | > and     |   |         |           |                               |   |
|   |   | > d       |   |         |           |                               |   |
|   |   | ecryption |   |         |           |                               |   |
|   |   | > key     |   |         |           |                               |   |
+---+---+-----------+---+---------+-----------+-------------------------------+---+
|   |   |           |   |         |           | > (send and receiver)         |   |
+---+---+-----------+---+---------+-----------+-------------------------------+---+

-   Used by cloud environments as data is saved in shared hardware

![](media/image17.jpeg){width="7.282638888888889in"
height="3.8361111111111112in"}

**Encryption Concepts**

> **Plaintext -** text, images or anything that can be read by a person
>
> **Algorithm** - code/maths which combined with an encryption key can
> encrypt plaintext -\>outputs **cypher text**
>
> **Key** - is a password
>
> **Cypher text** - encrypted data
>
> **Decryption** - taxes cyphertext and the key to output plain text

**Type of Keys:**

+----------------------------------+-----------------------------------+
| > **Symmetric encryption**       | > **Asymmetric encryption**       |
+----------------------------------+-----------------------------------+
| > • all entities use the same    | > • all entities use the same     |
| > algorithm                      | > algorithm                       |
+----------------------------------+-----------------------------------+
|                                  |                                   |
+----------------------------------+-----------------------------------+

![](media/image18.png){width="7.222916666666666in"
height="2.4715277777777778in"}

-   all entities have the same key

-   the key is transferred to all entities in a secure way

    -   transporting the key is a problem

    -   usually is transferred before the cypher text

```{=html}
<!-- -->
```
-   the entities agree on keys

    -   a public key

        -   used to generate cypher text

    -   a private key

        -   used to decrypt the cypher text

-   The key do not need to be exchanged in advance

    -   the reader needs to have the private key

    -   the writer needs just the public key

-   **Encryption does not prove identity**

-   Signing - using the private key, where the receiver uses the public
    key of the sender to check the signature

    -   is used to verify identity

    -   is called **key signing**

> ![](media/image19.png){width="6.585106080489939in"
> height="3.4506135170603676in"}
>
> ![](media/image20.png){width="6.613064304461942in"
> height="3.5425535870516187in"}
>
> **Signing :** it uses verify the descriptor is robot general or not.
>
> ![](media/image21.png){width="7.189583333333333in"
> height="3.5368055555555555in"}
>
> **Steganography**
>
> Sometimes encryption is not enough. Steganography is another layer of
> protection. Hiding a message within a picture, or something else.

![](media/image22.png){width="6.40361220472441in"
height="3.5744685039370077in"}

**IAM**

> Each account has a **root** user that has **full permissions** on the
> AWS accounts. - unrestricted access The **root** user cannot be
> restricted in anyway.
>
> Other accounts to have access to AWS account can be users, groups or
> applications. These accounts should be restricted to what they needs
> to achieve, and are called **least privilege access**.
>
> Every AWS accounts comes with a trusted **IAM** and its own database.
> This **IAM** belonging to the accounts, is an instance dedicated to
> **this** account, and is separated from the other AWS accounts.
>
> When a user is added, the account automatically trusts the new user as
> much as it trusts IAM.
>
> **IAM** allows to create policies for each users, group, role. These
> policies state what is allowed or restricted for each identity.
>
> IAM identities start with no permissions on an AWS Account, but can be
> granted permissions (almost) up to those held by the Account Root
> User.

![](media/image23.jpeg){width="7.30625in" height="3.432638888888889in"}

> **IAM** has 3 main jobs:

1.  CRUD identity (IDP)

2.  Authenticate identities

3.  Authorize identities. Allows them or denies them actions based on
    > authentication.

> **IAM** is:

-   free, but there are some limits.

-   is a local service, for the AWS account/infrastructure

-   controls what identities can do : allows/denies via policies

-   controls only local permissions

> There is limit of **5000 IAM user/account**
>
> **IAM** is a **global service** so this is a global limit
>
> An **IAM user** can be a member of maximum **10 groups**

**Create admin (IAM) user**

1.  click to IAM console

2.  click on user (left)

3.  click add user

4.  for an admin account, select the:

    a.  Attach existing policies

    b.  **AdministratorAccess**

> **This account now has the same privileges as the root user of the
> account, but is privileges can be restricted by the root user.**

**IAM Access Keys**

1.  user and password are required when using the AWS console

2.  access keys are required when using the terminal

> An IAM user has 1 user and 1 password, and it cannot have more than
> that.

-   **username** is public

-   **password** is private

-   **MFA** is private

> IAM Access Keys

-   **Access Key ID** - like a username

-   **Secret Access Key** - as password (can only be seen once and
    > cannot be changed)

> **Rotated Access Keys** - change the access keys (delete and create a
> new one)

-   can be used only by IAM **users** (roles can use one)

> **Create access keys:** (only 2 access keys can be on one user)

1.  go to security credentials

2.  create access key

> **Configure the terminal:**

+-------------------------------------------------+--------------------+
| > **aws configure \--profile                    | > configure a      |
| > name-of-the-profile**                         | > profile          |
+=================================================+====================+
|                                                 |                    |
+-------------------------------------------------+--------------------+
| > **aws s3 ls \--profile -management(name of    | > ls s3            |
| > profile)**                                    |                    |
+-------------------------------------------------+--------------------+
|                                                 |                    |
+-------------------------------------------------+--------------------+

**Identity Policies**

> IAM identities are users, groups and roles.
>
> **An IAM policy is a set of security statements. It grants or denies
> access to AWS products and features to any identity that uses that
> policy.**
>
> **Identity policies** also known as **policy documents**, are created
> using JSON.
>
> A policy document is one or more statements.
>
> Once an entity is authenticated, and AWS knows what policies an
> identity has.
>
> **A statement only applies if the interaction the identity has with
> the AWS matches the action and the resource.**
>
> A **statement has:**

-   **SID** (statement ID)

    -   optional filed

    -   identifies a statement

-   **Action**

    -   matches one or more actions

    -   it can be very specific

    -   service:action

    -   wildcards can be used to match all actions of a service S3:\*

    -   there are three options

        -   a specific individual action

        -   a wild card

        -   a list of multiple independent actions

-   **Resource**

    -   are the same as actions, but they match a **resource**

    -   matches individual AWS resources or a list of AWS resources,
        > wild cards are acceptable as well

-   **Effect**

    -   can be **allowed** or **denied**

    -   ![](media/image24.jpeg){width="6.7125in"
        > height="1.5069444444444444in"}allows a user or not to access a
        > resource and perform an action

```{=html}
<!-- -->
```
-   in the picture above, effect allowed and denied are granted over a
    > S3 bucket.

    -   in this case **overall access** is **allowed**, but
        > **constrained** on the catgifs bucket

-   **Explicit deny wins always**

-   ![](media/image25.jpeg){width="2.9555555555555557in"
    > height="1.4222222222222223in"}**Explicit allow** wins but not in
    > favor of **explicit deny**

-   **If an effect is not specified, than is implicit denied**

-   **By default a policy is DENIED**

-   **RULE: deny, allow, deny**

> **Inline policies** - are granted for each entity individuall

-   used for exceptions - special circumstances **Managed policy** - one
    > policy attached to many identities

-   AWS managed policies

-   customer managed policies - created by the owner

![](media/image26.png){width="6.267716535433071in"
height="3.5277777777777777in"}

**Policy Rule with Example:\
**

![](media/image27.png){width="6.267716535433071in"
height="3.5277777777777777in"}

## Inline And Managed Policy: 

Inline policies -

-   are granted for each entity individually

-   Used for exceptions - special circumstances

Managed policy -

-   one policy attached to many identities -

-   AWS managed policies - customer managed policies - created by the
    owner

![](media/image28.png){width="2.9218755468066493in"
height="1.7428729221347332in"}![](media/image29.png){width="3.088542213473316in"
height="1.7385826771653543in"}

![](media/image30.png){width="6.140625546806649in"
height="3.457926509186352in"}

**IAM Users and ARNs**

![](media/image31.jpeg){width="4.334027777777778in"
height="1.6368055555555556in"}

> These are called **PRINCIPLES**, and for the principles to be able to
> do anything it needs to authenticate and be authorized.
>
> The process is like this:

1.  the principle makes a request to IAM to access/interact resources

2.  the principle need to authenticate as an IAM used

> a\. can be achieved in two ways: **login credentials** or **access
> keys**

i.  **humans used login credentials**

ii. **applications use access keys**

```{=html}
<!-- -->
```
3.  Now the principle is an authenticated entity and can start
    > interacting with AWS

4.  AWS knows which polies applies to the identity **(authorization)**

> AMAZON RESOURCE NAME (ARN)
>
> **ARN are uniquely identify resources within any AWS accounts**
>
> **ARNs** can always identify single resources in the same account
> weather they are individual resources in the same account or different
> accounts.
>
> ARNs are used in IAM policies which are generally attached to
> identities such as IAM users, and they have a defined format.
>
> refers to the **actual bucket**

![](media/image32.jpeg){width="2.8333333333333335in" height="0.91875in"}

> refers to **all the objects in the bucket**

### **ARN structure:**

[arn:partition:service:region:account-id:resource-type/resource-id]{.underline}

Partition: aws-cn (aws-china-begin-region) \| aws

**Service: s3**

**Region:**

**Account-id:3423536**

**Resource:**

⇒ if service is Global service then no need to specify region:account-id

[arn:aws:s3:::catgifs/\*]{.underline}

![](media/image33.png){width="6.267716535433071in"
height="3.5277777777777777in"}

**IAM Groups**

> **IAM groups** are containers for IAM users.

-   you cannot login into a group

-   the group is used to manage policies easier for users

-   facilitates the management of IAM users

> An **IAM user** can be part of multiple **IAM groups!**

-   it does **not EXIT** by **default** a general **IAM Group** that
    > applies to all IAM users.

    -   if a group like this is needed, it needs to be created and
        > managed by the admin

-   **groups within groups does not exist**

-   **IAM groups** contain users

-   **IAM** groups contain permissions attached

-   **there is a limit of 300 groups/account** (can be extended by a
    > support ticket)

-   can hold identity permissions

-   admin groupings of IAM users

> Policies can be attached to resources

-   these policies can grant access to different IAM users

-   allows or denies access to IAM users to identities

-   id does this by referencing these identities using an ARN

-   a policy on a resource and reference IAM users and IAM roles by
    > using ARN

-   groups are not identities and cannot be referenced as principals in
    > a policy

    -   resources cannot grant access to IAM groups

**IAM Roles**

> A single **principle** uses an IAM user.
>
> **IAM roles** are also identities

-   used by multiple principles (not just one as users)

    -   they can be multiple AWS users

    -   they can me multiple external applications, users, etc.

-   if you cannot identify the number of principles that use an identify
    > then is a candidate for an IAM role

-   if you have more than 5000 users (the limit of IAM users) it can
    > also be a candidate for an IAM role

-   used on temporary basis

-   a role **represents a level of access inside an AWS account**

-   **an IAM user is a representation of a user for long term**

-   **a role borrows the permissions on a short period of time**

> **IAM** users have permission policies attached to them in inline or
> managed policies

-   these policies define what permission an identity gets inside AWS

> **IAM roles**

-   have two types of policies that can be attached to them

    -   trust policy

        -   which identities can assume the role

        -   can refer different identities: IAM users, other roles and
            > AWS services, identities in other AWS accounts

        -   if an identity is allowed, AWS generates temporary security
            > credentials (like access keys)

            -   they are time limited

            -   can be renewed

            -   the identities can access the resources specified in the
                > **permission policy**

    -   permission policy

        -   every time the temporary credentials are used are checked
            > against the permission policy **Roles** are real
            > identities, as IAM users, roles can be referenced in
            > resource policies.

-   are used in AWS organizations, allowing us to log into one account
    > in the organization and access different account without having to
    > login again

-   they are really useful when having a large number of accounts

> Temporary credentials, for roles, are generated by a service called
> Secure Token Service (STS). sts:AssumeRole
>
> **When and where to use IAM Roles**

+-------------------------------------------------------+--------------+
| > YES                                                 | > NO         |
+=======================================================+==============+
| > Services that need permissions                      |              |
+-------------------------------------------------------+--------------+
|                                                       |              |
+-------------------------------------------------------+--------------+
| > Anything that is not an identity                    |              |
+-------------------------------------------------------+--------------+
|                                                       |              |
+-------------------------------------------------------+--------------+
| > Very useful in emergency                            |              |
+-------------------------------------------------------+--------------+
| > situations                                          |              |
+-------------------------------------------------------+--------------+
| > \- break glass situation                            |              |
+-------------------------------------------------------+--------------+
| > \- used when absolutely                             |              |
+-------------------------------------------------------+--------------+
| > required                                            |              |
+-------------------------------------------------------+--------------+
|                                                       |              |
+-------------------------------------------------------+--------------+
| > When adding AWS in an existing                      |              |
+-------------------------------------------------------+--------------+
| > corporate environment                               |              |
+-------------------------------------------------------+--------------+
| > Roles are often used when you                       |              |
+-------------------------------------------------------+--------------+
| > want to reuse the existing                          |              |
+-------------------------------------------------------+--------------+
| > identities for use in AWS                           |              |
+-------------------------------------------------------+--------------+
| > \- external accounts cannot                         |              |
+-------------------------------------------------------+--------------+
| > be used directly                                    |              |
+-------------------------------------------------------+--------------+
| > \- allowing a role to be                            |              |
+-------------------------------------------------------+--------------+
| > assumed by an external                              |              |
+-------------------------------------------------------+--------------+
| > account (or multiple)                               |              |
+-------------------------------------------------------+--------------+
| > \- called ID federation                             |              |
+-------------------------------------------------------+--------------+
|                                                       |              |
+-------------------------------------------------------+--------------+
| > Giving access to users of an app,to some resources  |              |
| > -called web identity federation                     |              |
+-------------------------------------------------------+--------------+
|                                                       |              |
+-------------------------------------------------------+--------------+

Hardcoding access keys is not advisable as is a security concern, and
whenever the keys change, they need to be hardcoded again.

In this scenario, the **IAM Role** is the perfect solution.

**AWS Organizations**

> **AWS Organizations** is a product that **allows companies to manage
> multiple AWS accounts** in a cost-effective way.
>
> An account is needed to create an organization.
>
> The account that creates the AWS account, becomes the management
> account for that organization.
>
> The management account is also called master account.
>
> Using the management account

-   you can invite other standard AWS accounts into the organization

    -   the invited standard AWS accounts need to accept the invitation
        > to the organizations

    -   if the standard AWS accounts accept the invitation they become
        > part of the organization

    -   these accounts are changed from being standard AWS accounts to
        > **member accounts of that organization**

-   an organization has **only one** master accounts, and **zero or more
    > member accounts**

-   **the organization can create accounts directly within it**

    -   it isn\'t an invite process

-   with organizations, IAM users do not need to exit within each member
    > AWS account

    -   IAM roles can be used to allow IAM users to access other AWS
        > accounts

> The Organization has a hierarchy (like a reverted tree)

-   the **root container** of the organization is at the top of the tree

    -   do **not** confuse it with the **root user**

-   other containers can be created - known as **organizational units
    > (OUs)**

> Organizational billing

-   the billing method for each member account are removed

-   the member accounts pass their billing through the management
    > account of the organization also called **payer account**

-   the single monthly bill generated for AWS organization, covers all
    > the accounts of the organization

> The organization has a service called Service Control Policies (SCPs)

-   this service can restrict what each member account can do

**Service Control Policies (SCP)**

> SCP is a feature of AWS organizations, which can be used to restrict
> AWS accounts.
>
> **SCP** is a JSON document (policy document) and can be attached to
> the

-   organization as a whole

    -   by attaching them to the root container

-   one or more organizational units (OU)

-   to individual AWS accounts

> Service Control Policies inherit down the organizational tree.

-   if the are attached to the organization it affects all accounts
    > within the organization

-   if they are attached to an organizational unit, they impact all the
    > account inside the organizational unit

    -   if there are nested OUs , it will affect the OUs inside the
        > organization as well

> The management account of the organization is special. If this account
> has policies attached directly, or through an organization unit, **the
> management account is not affected by any SCP!**
>
> Service Control Policies are account permission boundaries and they
> limit what an account can do.
>
> **As mentioned before, we cannot restrict the account root user of an
> AWS account, but within an organization with the SCP we can restrict
> what an AWS account can do (with all the entities in that account)!**
> Therefore, restricting indirectly the account root user.
>
> **SCP** do not grant any permissions, they define the limit of what
> isn\'t allowed (and what is). You still need to give the identities in
> that AWS account permissions to AWS resources, **but SCPs will limit
> the** **permissions that can be assigned to individual identities.**
>
> SCPs can be used in two ways:

1.  Block by default and allow certain services: using an allow list

2.  Allow by default and deny certain services: using a deny list
    > (default)

> When SCP is enabled in an account, AWS applies a default policy which
> is called a **full AWS access. This is applied to all OUs within the
> organization. - nothing is restricted**

-   **this maintains the current functionalities in the organization (in
    > the moment of creating the SCP )**

> To use the allow list, the **FULL AWS access** list must be removed,
> and allowed services should be specified independently into a new
> policy. - **security improved**
>
> **SCP do not grant access to anything, they specify WHAT CAN AND
> CANNOT BE ALLOWED by identity policies within that account**
>
> **Only what is allowed in the SCP and the identity policies is
> actually allowed.**

**Policy Interpretation Deep Dive**

1.  identify how many statements make up the policy document

    -   each document has a single statement or a list of statements

        -   a list of statements has **\[ {statement}, {statement},
            > {etc} \]**

2.  identify what each statement actually does

    -   each statement has an **effect** which is **allowed** or
        > **denied**

        -   this states if that certain statement **allows** or
            > **denies** a set of **activates**

3.  start with the **ALLOWED** statements

4.  end with **DENIED** statements

5.  **check for NOT operations**

![](media/image34.jpeg){width="0.12361111111111112in" height="0.125in"}

> The priority orders is **Deny, Allow, Deny**

-   **by default is denied** - no permissions

    -   if a permission is not explicitly allowed in the policy is by
        > default denied

-   **if something is denied explicitly [that always wins]{.underline}**

-   **if something is allowed explicitly then is allowed, [unless is
    > ALSO denied]{.underline}**

-   **if something is no explicitly denied or allowed, than is
    > implicitly by default denied**

![](media/image34.jpeg){width="0.12361111111111112in" height="0.125in"}

> **if conditions are present in a statement, the statement applies only
> if the condition is a met**

![](media/image34.jpeg){width="0.12361111111111112in" height="0.125in"}

> **if a policy contains only a DENY, is usually used with another
> policy, as a single DENY will do nothing to permissions, as by default
> permissions are DENIED**
>
> **{**
>
> **\"Version\": \"2012-10-17\",**
>
> **\"Statement\":**
>
> **\[**
>
> **{**
>
> **\"Effect\":\"Allow\",**
>
> **\"Action\":\[**
>
> **\"s3:PutObject\",**
>
> **\"s3:PutObjectAcl\",**
>
> **\"s3:GetObject\",**
>
> **\"s3:GetObjectAcl\",**
>
> **\"s3:DeleteObject\"**
>
> **\],**
>
> **\"Resource\":\"arn:aws:s3:::holidaygifts/\*\"**
>
> **},**
>
> **{**
>
> **\"Effect\": \"Deny\",**
>
> **\"Action\": \[**
>
> **\"s3:GetObject\",**
>
> **\"s3:GetObjectAcl\"**
>
> **\],**
>
> **\"Resource\":\"arn:aws:s3:::holidaygifts/\*\",**
>
> **\"Condition\": {**
>
> **\"DateGreaterThan\": {\"aws:CurrentTime\":
> \"2020-12-01T00:00:00Z\"},**
>
> **\"DateLessThan\": {\"aws:CurrentTime\": \"2020-12-25T06:00:00Z\"}**
>
> **}**
>
> **}**
>
> **\]**
>
> **}**
>
> **check for NOT operations**
>
> **{**
>
> **\"Version\": \"2012-10-17\",**
>
> **\"Statement\": \[**
>
> **{**
>
> **\"Sid\": \"DenyNonApprovedRegions\",**
>
> **\"Effect\": \"Deny\",**
>
> **\"NotAction\": \[**
>
> **\"cloudfront:\*\",**
>
> **\"iam:\*\",**
>
> **\"route53:\*\",**
>
> **\"support:\*\"**
>
> **\],**
>
> **\"Resource\": \"\*\",**
>
> **\"Condition\": {**
>
> **\"StringNotEquals\": {**
>
> **\"aws:RequestedRegion\": \[**
>
> **\"ap-southeast-2\",**
>
> **\"eu-west-1\"**
>
> **\]**
>
> **}**
>
> **}**
>
> **}**
>
> **\]**
>
> **}**
>
> **{**
>
> **\"Version\": \"2012-10-17\",**
>
> **\"Statement\": \[**
>
> **{**
>
> **\"Effect\": \"Allow\",**
>
> **\"Action\": \[**
>
> **\"s3:ListAllMyBuckets\",**
>
> **\"s3:GetBucketLocation\"**
>
> **\],**
>
> **\"Resource\": \"\*\"**
>
> **},**
>
> **{**
>
> **\"Effect\": \"Allow\",**
>
> **\"Action\": \"s3:ListBucket\",**
>
> **\"Resource\": \"arn:aws:s3:::cl-animals4life\",**
>
> **\"Condition\": {**
>
> **\"StringLike\": {**
>
> **\"s3:prefix\": \[**
>
> **\"\",**
>
> **\"home/\",**
>
> **\"home/\${aws:username}/\*\"**
>
> **\]**
>
> **}**
>
> **}**
>
> **},**
>
> **{**
>
> **\"Effect\": \"Allow\",**
>
> **\"Action\": \"s3:\*\",**
>
> **\"Resource\": \[**
>
> **\"arn:aws:s3:::cl-animals4life/home/\${aws:username}\",**
>
> **\"arn:aws:s3:::cl-animals4life/home/\${aws:username}/\*\"**
>
> **\]**
>
> **}**
>
> **\]**

**}**

-   **List everything inside buckets**

```{=html}
<!-- -->
```
-   **List a specific bucket - animals4life**

    -   **no prefix**

    -   **all home/ prefix**

    -   **only the buckets that match the name of the IAM user using**

> **the policy and everything inside that bucket -** and no other
> \"folders\"

-   **Allows any operation, as long as the prefix matches
    animals4life/home/iamusername - on the folder and inside it**

**Policy Evaluation Logic**

+-----------------------------------------------+-----------------------+
| Tuesday, July 13, 2021                        | > 11:19 AM            |
+===============================================+=======================+
+-----------------------------------------------+-----------------------+

> **Security architecture can have multiple levels of identities and
> account boundaries, and even multiple AWS accounts.**
>
> When evaluating effective permissions, there a few components
> involved:

1.  consider any AWS organization service control policies

    -   this impact what identities inside an organization can do

2.  consider the resource policies

3.  IAM identity boundaries

4.  session policies - what a role is allowed

5.  identity policies

> Handling permissions - same account

-   AWS gathers all policies which apply to an identity accessing a
    > particular resource

    1.  **EXPLICIT DENY -** searching for an **explicit deny** in what
        > the identity is trying to do with a certain resource or
        > service

        -   if there are explicit deny then, the actioned is denied

        -   if there is no explicit deny then the processing continues

    2.  **SERVICE CONTROL POLICY -** if there are no explicit denies,
        > then service control policies (SCP - part of the organization
        > product) are processed

        -   if service control policies exist, then they are checked if
            > they allow the action

        -   if the service control policy allows or if the service
            > control policy does not exist, then the processing
            > continues

        -   if the service control policy does not allow the process,
            > then the access is not permitted

    3.  **RESOURCE POLICY** - if the resource policy contains an
        > **allow** then the actioned is allowed

        -   otherwise, the processing continues

    4.  **PERIMISSION BOUNDARY** - following the same process

        -   if there is a no boundary or if the actioned is allowed then
            > processing continues

        -   if the a boundary exists and denies the action then
            > processing stops, and the action is denied

    5.  **SESSSION POLICY -** is checked if a role is used

        -   if the action is not explicitly allowed, then is implicitly
            > denied and the processing stops denying the action

        -   if there is session policy, or if there is one allowing the
            > action then processing moves on

    6.  **IDENTITY POLICY**

        -   if the action is explicitly allowed then the action is
            > permitted

        -   if the action is explicitly denied then the action is denied

        -   by default any action is **denied**

![](media/image35.png){width="7.163888888888889in"
height="10.002083333333333in"}

> Handling permissions - multiple accounts

![](media/image36.jpeg){width="6.847916666666666in"
height="3.432638888888889in"}

**Cloud HSM**

+-----------------------------------------------+----------------------+
| Tuesday, July 13, 2021                        | > 12:38 PM           |
+===============================================+======================+
+-----------------------------------------------+----------------------+

> **Cloud HSM** is a **cloud**-hosted Hardware Security Module (**HSM**)
> service that allows you to host encryption keys and perform
> cryptographic operations in a cluster of FIPS 140-2 Level 3 certified
> HSMs. Google manages the **HSM** cluster for you, so you don\'t need
> to worry about clustering, scaling, or patching.
>
> KMS
>
> KMS is the key management service within AWS

-   used for encryption within AWS and integrates with other AWS
    > products

    -   generates keys

    -   manages keys

-   but has one security concern - it is a shared service

    -   your part of KMS is isolated under the cover it is shared with
        > other accounts

    -   while the permissions in AWS are strict, AWS has a certain level
        > of access to the KMS product - they manage the hardware and
        > software which provides the KMS product to its customers

-   behind the scenes KSM uses HSM (Hardware Security Model) - industry
    > standard pieces of hardware which are designed to manage keys and
    > perform cryptographic operations

-   is **Level 2 - some Level 3**

-   all operations are performed with AWS standard API, and all
    > permissions are controlled with IAM permissions

> HSM

![](media/image37.png){width="0.16805555555555557in"
height="4.608333333333333in"}

> **HSM** is a TRUE \"SINGLE TENANT\" Hardware Security Module (HSM)

-   Cloud HSM - hosted by AWS

    -   HSM is hosted by AWS and they are reasonable for hardware
        > maintenance

    -   **they have no access to the part of the unit where the keys are
        > stored and managed**

    -   is not very integrated with AWS

> ![](media/image38.jpeg){width="0.16666666666666666in"
> height="0.16666666666666666in"}^▪^ you access it with Industry
> Standard API: PKCS 11, Java Cryptography Extensions (JCE), Microsoft
> CryptoNG (CNG)

-   On-Premise HSM Device

> ![](media/image39.jpeg){width="0.16666666666666666in"
> height="0.14583333333333334in"}- is **FIPS 140- 2 Level 3**
>
> Architecture
>
> **Cloud HSM** are not deployed inside a VPC that you control. They are
> deployed into an AWS managed **Cloud HSM VPC ,** that you have no
> visibility of.

![](media/image40.png){width="7.353472222222222in"
height="10.002083333333333in"}

> ![](media/image38.jpeg){width="0.16666666666666666in"
> height="0.16666666666666666in"}Overlaps
>
> A feature from KMS called **Custom Key Store**, which can use **Cloud
> HSM** to get many benefits from Cloud HSM and integration with AWS.
>
> When to be used

-   there is no integration between AWS standard APIs and HSM

-   HSM can be used to perform client side encryption

    -   encrypt on local device and then upload the encrypted object to
        > AWS

-   HSM can be used to offload the SSL/TLS processing for Web Servers

    -   the server does not need the perform those cryptographic
        > operations

    -   accelerates the process

-   enables Transparent Data Encryption (TDE) for different products
    > such as Oracle Databases

-   the client is responsible for managing the keys, and the encryption
    > operations

-   can be used to protect and manage Private Keys for Certificate
    > Authorities (CA)

> ![](media/image38.jpeg){width="0.16666666666666666in"
> height="0.16666666666666666in"}- **the overall theme is that anything
> that isn\'t specific to AWS, anything which expects to have access to
> a hardware security module using Industry Standard APIs, then the
> ideal product for that is Cloud HSM**

-   **for anything using standards, for anything that has to integrate
    > with products which aren\'t AWS then Cloud HSM is ideal**

-   **for anything that requires AWS integration, then natively cloud
    > HSM isn\'t suitable**

**CloudWatch**

+-------------------------------------------------+--------------------+
| Tuesday, June 22, 2021                          | > 1:46 PM          |
+=================================================+====================+
+-------------------------------------------------+--------------------+

> **Cloud Watch** is a support service used by almost all AWS services -
> especially for operational services and monitoring.
>
> Cloud watch performs three main jobs:
>
> It collects and manages operational data

a.  data that is generated by an environment

```{=html}
<!-- -->
```
1.  a collection of metrics, monitoring of metrics and actions based on
    > metrics

    a.  data relating to AWS products

        i.  CPU utilization of EC2

        ii. numbers of visitors

2.  Cloud Watch logs

    a.  logging data

3.  Cloud Watch events

    a.  EC2 terminated, started or stop

    b.  schedule an event

![](media/image41.jpeg){width="6.7375in" height="2.775in"}

> Namespace

-   is a container for monitoring data, separating things in different
    > areas

-   all AWS data go into a namespace is **AWS/service** (e.g. AWS/EC2)
    > **Metric** is a collection of related datapoints in a time ordered
    > structure.

-   CPU utilization

-   network in an out

-   disk utilization

-   will start monitoring when the service is started, and it will stop
    > when the service is disabled

> **Datapoints**

-   consists of two things:

    -   time when measurement was conducted

    -   and a value that represents the monitoring

> **Dimension**

-   are name value pairs which allow CloudWatch to separate things

![](media/image42.png){width="6.9534722222222225in"
height="10.002083333333333in"}

> **Alarms**

-   are created and linked to a specific metric

-   based on the alarm\'s configuration, an action can be performed if
    > the condition for the alarm is met

**CloudWatch Logs**

+----------------------------------------------+-----------------------+
| Friday, July 2, 2021                         | > 1:22 PM             |
+==============================================+=======================+
+----------------------------------------------+-----------------------+

> **CloudWatch logs** is a public service. It has an endpoint in which
> applications connect to is hosted in the AWS public zone.

-   which means you can used the product within the AWS VPCs or from
    > on-premises environments and even other cloud platforms as long as
    > you have internet and permissions

-   allows you to **store, monitor** and **access** logging data

    -   logging data is a piece of information data, and a timestamp

-   has some built in integrations with AWS services such as EC2, VPC
    > flow logs, lambda, CloudTrail, R93 and more

-   each service that interacts with CloudWatch can store data directly
    > inside the product

-   AWS services can log into CloudWatch directly

-   unified CloudWatch agent can be used to integrate outside services

-   can generate metrics based on logs using the **metric filter**

-   **is a regional service**

-   **log streams** is a collection of log events [from the same
    > source]{.underline}

-   **log groups** are containers for multiple log streams for the [same
    > type of logging]{.underline}

    -   in log groups settings are located as well

        -   this settings apply to all log streams inside that group

    -   metric filters are defined here as well

![](media/image43.png){width="0.6916666666666667in"
height="9.027777777777777e-3in"}![](media/image44.jpeg){width="7.394444444444445in"
height="3.547222222222222in"}

-   has two sides:

> ![](media/image45.jpeg){width="0.15138888888888888in"
> height="0.125in"}○ **ingestion** side

-   is concerned to getting logs into the system

-   is a public service

-   designed to store, monitor and access logging data

-   work with AWS, on-premises, IOT any other application

-   **cloud log agent** is required for system or custom application
    > logging

-   can ingest logging from VPC flow logs, CloudTrail, lambda, route53
    > etc.

![](media/image46.jpeg){width="0.15138888888888888in"
height="0.15347222222222223in"}

> **Log events** will be collected in **log streams** if they are coming
> from the same source **Log groups** are a **collection of log
> streams**

![](media/image47.png){width="5.823611111111111in"
height="10.002083333333333in"}

> On **Log Groups** retention, permissions and encryption are set.
>
> **Metric Filter** is a log group filter

-   is looking for patterns in all log streams within a log group

-   a **metric** is created from a metric filter

-   can be used to generate alarms

> ![](media/image48.jpeg){width="0.15347222222222223in"
> height="0.15347222222222223in"}^▪^ Logs can be exported with

-   S3 export

    -   is a manual process

    -   takes up to 12 hours - **is no real time**

    -   can only be encrypted with SSE-S3

> ![](media/image46.jpeg){width="0.15138888888888888in"
> height="0.15347222222222223in"}○ **subscription** side

-   what other products can use those logs for other activities

-   to export logs:

    -   Kinesis Data Firehose

        -   allows near real-time delivery of logging data to S3

        -   is cost affective as long

    -   AWS Managed Lambda Function

        -   allows logging data delivered in real-time to Elasticsearch

        -   real time

    -   custom Lambda function

        -   deliver in the chosen resource

        -   ![](media/image49.jpeg){width="6.220833333333333in"
            > height="2.9256944444444444in"}real time

> Summary

![](media/image50.jpeg){width="0.15347222222222223in"
height="0.15138888888888888in"}for any log management solutions by
default the **CloudWatch Logs** should be used

-   for AWS or on-premises systems

![](media/image51.jpeg){width="0.15347222222222223in"
height="0.15347222222222223in"}

> logs can be exported using

-   S3 using CreateExportTask

    -   takes up to 12 hours

    -   is not real time

-   Kinesis Firehose

    -   near real-time

    -   can export logs on S3 or other destinations

-   subscription filter configured through Lambda or Kinesis Data stream

    -   is real time

-   Elasticsearch

    -   using AWS Managed Lambda to deliver logging data

    -   is real time

```{=html}
<!-- -->
```
-   Metric functionality takes incoming data and performs searches on
    > that data, generate a metric to push notifications or start an
    > event driven architecture

**CloudWatch Architecture**

+-------------------------------------------------+--------------------+
| Monday, August 2, 2021                          | > 2:33 PM          |
+=================================================+====================+
+-------------------------------------------------+--------------------+

> **Cloud Watch** is a product that ingest, store and manage metrics

-   is a **public service**

-   any service using CloudWatch need to have access to the public
    > endpoint

-   many AWS services include native management plane integration

    -   EC2 for example provides CloudWatch metrics without by default

-   the cloud watch **agent** which can communicate back to the service

    -   provides details of running processes , CPU usage, memory usage,
        > etc.

    -   certain services **require the agent, the API** or a combination
        > **of both**

-   once the data is inside CloudWatch **is stored in a persistent way**

    -   you can interact with it via de console UI, the command line or
        > via APIs

    -   provides dashboards and anomaly detection

-   provides a features called **alarms**

    -   they react to metrics based on conditions

    -   the alarm can be in the **OK state** or the **alarm state**

    -   if the data breaches normal levels notifications can be sent

> **ORANGE** - public zone
>
> **RED -** on premises virtual machines and application, internet
> connected application **GREEN** - private zone

![](media/image52.jpeg){width="5.425694444444445in"
height="2.682638888888889in"}

> Data
>
> **Namespace**

-   **is a container for metrics within CloudWatch**

    -   AWS/EC2 or AWS/Lambda

    -   this separates the metrics from different services

> **Datapoint**

-   are the smallest components of CloudWatch

-   they have a value, a time stamp and a unit of measure

> **Metric**

-   **is a time ordered set of data points**

-   can include CPU utilization, network in, dick writes bytes for EC2

-   has a name and a namespace

> **Dimension**

-   **is a name value pair which is provided when you add data points
    > into Cloud Watch**

-   differentiates between instances where **name= \"instanceID\"** and
    > **value=actual_instance_ID**

-   can be used to aggregate data such as viewing statistical data for
    > different types of instance across

> an entire region
>
> **Resolution**

-   metrics provided by AWS services by default use **standard
    > resolution**

    -   they have 60 seconds granularity

    -   high resolution metric costs more - 1 second resolution

    -   metric resolution has 1 second, 5 seconds, 10 seconds, 30
        > seconds and any multiple of 60 seconds

        -   minimum time period for one particular data point

    -   retains data for a certain period of time

        -   for less then 60 seconds data is retained for 3 hours

        -   for 60 seconds data is retained for 15 days

        -   for 300 seconds data is retained for 63 days

        -   for 3600 seconds data is retained for 455 days

    -   as data ages its aggregated and stored for **longer** with
        > **less resolution**

        -   **minimum, maximum, sum, average**

    -   percentile indicates the relative standing value of a set

> Alarms

-   can be created to monitor or watch a given metric over a specified
    > period

-   reading the data an alarm can be an **OK state** or an **alarm
    > state**

    -   based on the value of the metric versus a threshold defined

-   can be configured with one or more actions

    -   which can initiate actions on your behalf

**AWS X-Ray**

+-------------------------------------------------+--------------------+
| Sunday, August 8, 2021                          | > 1:16 PM          |
+=================================================+====================+
+-------------------------------------------------+--------------------+

> **AWS X-Ray** is a distributed tracing application

-   it is designed to track sessions through an application

    -   an app can be any kind: monolithic, serverless or distributed

-   takes data from all separate services and gives back **one single
    > overview** of the session flow of the application

> Concepts

-   **tracing header** - a tracing ID is generated and inserted into a
    > tracing header

    -   is using the header that the request is tracked through all of
        > the supported services of the application

    -   the supported services send data though the X-Ray service using
        > segments

        -   **segments** are data blocks and they detail:

            -   the host name and its IP

            -   requests and responses

            -   the user agent and client address

            -   the path

            -   the start and end time

            -   issues encountered

            -   can contain **sub-segments** which are a more granulated
                > version of the above explanation

    -   the X-Ray collects all the individual segments to provide and
        > end-to-end flow for a specific request

    -   the X-Ray generates a **service graph**

        -   an overall structure of how the application components fit
            > together

            -   shows how components work together

-   the X-Ray uses the graph and the collected data to generate a
    > service map which is **a visual representation of the graph**

-   **it needs IAM permissions**

**VPC Flow Logs**

+-------------------------------------------------+--------------------+
| Sunday, August 8, 2021                          | > 2:21 PM          |
+=================================================+====================+
+-------------------------------------------------+--------------------+

> **VPC Flow Logs** are a diagnostic tool for complex networks within
> AWS ![](media/image53.jpeg){width="0.15833333333333333in"
> height="0.13541666666666666in"}- they only capture packet Metadata

-   the source IP address

-   the destination ports

-   packet size

-   allow or deny

> ![](media/image54.jpeg){width="0.15833333333333333in"
> height="0.14583333333333334in"}- they **do not** capture packet
> contents
>
> Monitoring:

-   can monitor every network interface in a VPC

-   can monitor to subnet/s which monitor every network interface in
    > that subnet only

-   can be directly applied to network interfaces

    -   it is a hierarchy (downwards only):

        -   when a VPC its monitored, its subnets and interfaces are
            > monitored

        -   when a Subnet its monitored, its interfaces are monitored

-   are not real-time

-   its destination can be **S3** of **CloudWatch log**

![](media/image55.jpeg){width="5.68125in" height="2.785416666666667in"}

-   they do not log all traffic, there are some things which are
    > excluded

    -   communication with the Metadata IP

    -   AWS time synchronization server

    -   DHCP traffic

    -   any communication with the Amazon Windows licensing server

![](media/image56.jpeg){width="5.590972222222222in"
height="2.2291666666666665in"}

**CloudTrail Essentials**

> Almost everything that can be done with an AWS account can be logged
> with CloudTrail product.
>
> CloudTrail:

-   logs APIs calls and account activities

    -   each is called a **CloudTrail event**

        -   is an activity in an AWS account

        -   an activity is an action taken by an user, role or a service

-   by default logs the last 90 days activity in the CloudTrail Event
    > history

    -   is enabled by default

    -   is free

    -   can be customized

-   can be two types

    -   **management events** (by default the CloudTrail only logs this)

        -   provides information about operations performed on resources
            > (control)

    -   **data events** (not enabled by default)

        -   contains information about resource operations performed on
            > or in a resource

-   stored the events in a definable S3 bucket (only if you configure a
    > trail, otherwise you don\'t get an S3 bucket)

    -   stored in JSON format

-   a **CloudTrail trail** is a unit of **configuration** within the
    > CloudTrail product

    -   how configuration is done

    -   **a trail logs events for the AWS region that it\'s created in**

    -   a trail can be configured for one region, or for all regions.

-   can be integrated with CloudWatch logs

    -   in addition of adding into the S3 buckets dedicated for events,
        > it adds it to the CloudWatch logs

-   it is **not real-time** - has a delay (15 minutes)

-   an organizational CloudTrail is available

    -   can be created from the management account of the organization

    -   can store all the information from **all the accounts** within
        > the organization

> AWS services are largely split up into regional services and global
> services. So when this different type of services log to CloudTrail
> they either log in the region the event is generated in, or if **they
> are** global (IAM, STS, CloudFront) they log into **us-east-1**. A
> trail needs to be enabled to capture that data!
>
> ![](media/image57.png){width="6.5in" height="4.0625in"}

**Control Tower**

-   ﻿﻿Quick and Easy setup of multi-account environment

-   ﻿﻿Orchestrates other AWS services to provide this functionality.

-   ﻿﻿Control Tower uses Organizations, AM Identity Center,
    CloudFormation, Config and more\....

-   ﻿﻿**Landing Zone** - multi-account environment

-   ﻿﻿\... SSO/ID Federation, Centralised Logging & Auditing

-   ﻿﻿**Guard Rails** - Detect/Mandate rules/standards across all accounts

-   ﻿﻿**Account Factory** - Automates and Standardises new account
    creation.

-   ﻿﻿**Dashboard** - single page oversight of the entire environment

Control tower setup the sso

![](media/image58.png){width="6.5in" height="3.5340277777777778in"}AWS
Control Tower - Landing Zone

-   ﻿﻿.. built with AWS Organizations, AWS Config, CloudFormation

-   ﻿﻿**Security OU** - Log Archive & Audit Accounts (**CloudTrail &
    Config Logs)**

-   ﻿﻿**Sandbox OU** - Test/less rigid security

-   ﻿﻿You can create other OU\'s and Accounts

-   ﻿﻿AM Identity Center (**AWS SSO**) - SSO, multiple-accounts, ID
    Federation

-   ﻿﻿*Monitoring and Notifications - **CloudWatch and SNS***

AWS Control Tower - Guard Rails

-   Guardrails are rules - multi-account governance

-   There are 3 types of Guard Rails: **Mandatory, Strongly Recommended
    or Elective**

```{=html}
<!-- -->
```
-   There are 2 functions:

1.  Preventive - Stop you doing things (AWS ORG SCP)

    a.  enforced or not enabled (i.e allow or deny regions or disallow
        bucket policy changes)

    b.  it stop those things

2.  Detective - compliance checks (AWS CONFIG Rules)

    a.  clear, in violation or not enabled(detect CloudTrail enabled or
        EC2 Public IPV4)

    b.  it only identify the things

AWS Control Tower - Account Factory

-   ﻿﻿Automated Account Provisioning

-   ﻿﻿.. cloud admins or end users (with appropriate permissions)

-   ﻿﻿Guardrails - automatically added

-   Account admin given to a named user (IAM Identity Center)

-   Account & network standard configuration

-   Accounts can be closed or repurposed

-   Can be fully integrated with a businesses SDLC

**S3 Buckets**

> Simple storage service - S3
>
> **S3** is:

-   global storage platform - regional resilient

-   is a public service

-   unlimited data

-   multi-user access

-   any type of data

-   is economical

-   **default** storage on AWS

    -   **objects** - any data

    -   **buckets -** containers for objects

> **Objects** are files, made of:

-   object **key** (file name)

-   object **value** (the content of the file being stored)

-   size range from 0MB to 5TB/object

> ![](media/image59.png){width="3.9354844706911636in"
> height="2.2136843832020996in"}
>
> **Buckets**

-   **all buckets by default are private**

-   data inside the bucket has a primary region (than can be changed)

-   data never leaves the region (unless configured)

-   **the name of the bucket needs to be unique across all regions in
    > AWS**

-   can hold unlimited number of objects (object sizes 0 bytes to 5TB)

-   has a flat structure - all files are saved on the root file (no
    > folders in folders)

    -   the user can save folders in folders, but in reality is a **flat
        > structure**

    -   folders **are called prefixes**

-   **bucket names needs to be**

    -   all lower case

    -   no underscores

    -   3 - 63 characters - characters or digits

-   there is a limit of number of buckets for an AWS account, and **it
    > is a soft 100, and a hard limit 1000**

-   is good for large scale, data storage, distribution or upload

-   Can\'t be IP formatted e.g. 1.1.1.1

> **Simple Storage S3 - is an AWS Public Service, is an object storage
> system and buckets can store an unlimited amount of data**

S3 Patterns and Anti-Patterns :

![](media/image60.png){width="6.717361111111111in"
height="2.504861111111111in"}

**S3 Security**

> **S3** is private by default

-   by default the account root user has access to the bucket only

-   any other permissions need to be explicitly granted through:

    -   **[resource policy]{.underline}** - **who can access a
        > resource**

-   can grant access to identities from other accounts - (other AWS
    accounts)

can allow or deny anonymous principals - (sharing a bucket with the
world)

![](media/image61.jpeg){width="3.2055555555555557in"
height="1.8833333333333333in"}

-   **principal filed defines what principals have access to a
    > resource**

    -   **if is there, then it is a resource policy**

```{=html}
<!-- -->
```
-   **identity policy** - **what resources the identity can access**

    -   access can be granted to identities in your account only

> Bucket policies
>
> Can be used:

-   to control who can access objects (even targeting IP addresses)

![](media/image62.jpeg){width="4.384027777777778in"
height="3.0340277777777778in"}

> this permission allows only identities from 1.3.3.7, otherwise the
> statement
> applies!([link](https://repost.aws/knowledge-center/block-s3-traffic-vpc-ip#:~:text=The%20following%20example%20bucket%20policy%20blocks%20traffic%20to%20the%20bucket%20unless%20the%20request%20is%20from%20specified%20private%20IP%20addresses%20(%20aws%3AVpcSourceIp)%3A))

-   is a type of **resource policy** is applied to a bucket

-   a bucket can have **only one policy** but it can **have multiple
    > statements**

-   when an entity accesses a bucket, both the identity and the bucket
    > policy apply

Access Control Lists (ACLs)

**(not really used anymore)(not recommended)**

-   ![](media/image63.png){width="6.106944444444444in"
    > height="10.002083333333333in"}is a way to apply security to
    > objects and buckets

-   is a sub resource

-   they are inflexible and allow very simple permissions

-   you can use one ACL for multiple objects

    -   one ACL per object and one ACL per bucket

> Block Public Access

-   Adds another level of security, which apply no matter what the
    > **bucket policy says**.

    -   the Apply only for public access

    -   the do not apply to AWS identities

![](media/image64.jpeg){width="5.250694444444444in"
height="3.884027777777778in"}

**S3 Static Website Hosting**

> **S3 Static Website Hosting** allows access to buckets and object via
> HTTP.

-   when enabling it, you need to set an **index** and an **error**
    > document

    -   index home page - default page

    -   error page - is accessed when something goes wrong

-   needs to be HTML

-   if you use a domain than the bucket name needs to match the
    > domain\'s name

-   the default endpoint is influenced by the bucket name and the region
    > is in

> **Offloading**

-   if a website needs a database to load static media (images), S3
    > bucket can be used to store the media and retrieve it when needed
    > it

-   this is cheaper than other compute services as it is
    > costumed-designed for the storage of large data at scale

> **Out of band pages**

-   another services used, in case the main server is offline or has any
    > other interruptions, then we can change our DNS and point
    > customers at a backup static website hosted on S3

![](media/image65.png){width="6.5in" height="3.65625in"}

**Object Versioning and MFA Delete**

> [Object Versioning]{.underline}
>
> Object versioning starts up at the object level and is disabled by
> default. Once the object versioning is **enabled it cannot be enabled
> again, it can only be suspended and re-enabled again.**

![](media/image66.jpeg){width="6.98125in" height="3.1972222222222224in"}

> Without versioning enabled on a bucket, each object is identified
> solely by the object key, its name (which is unique inside the
> bucket). If an object is modified, the new version of the object
> replaces the old one.
>
> **Versioning allows** to store multiple versions of the same object
> within a bucket. **Any operation that modify objects will generate a
> new version of that object.**

-   The latest version of an object is called **the current object** or
    **latest version.**

-   When requesting an object from a version bucket, and no version is
    specified then the current version is returned. Other versions can
    be requested by **specifying the ID**.

> When an object is deleted in a version bucket, the current version of
> the object is marked as deleted, but the actual object is just hidden.
> **The delete marker is a special version of an object which hides all
> previous versions of that object.**
>
> The delete marker can be deleted, which results in restoring the last
> current version of that object.

![](media/image67.png){width="2.3161286089238846in"
height="1.3028641732283464in"}
![](media/image68.png){width="2.326447944006999in"
height="1.3086712598425196in"}

![](media/image69.png){width="7.139996719160105in"
height="10.017466097987752in"}

> **To truly delete an object, the version ID needs to be specified.**
> If the current version of the object is deleted, and there are other
> versions of that object present, the most current version before the
> current version becomes the current version object.
>
> Space within an bucket **is consumed by all the versions of objects**.
> (being billed for all). Even if you suspend the version service, the
> objects and their version withing that bucket are billed.
>
> **For zero costs, the bucket should be deleted.**
>
> MFA Delete (multi factor auth)
>
> MFA Delete is enabled within the versioning configuration of a bucket.

-   when is enabled it means that MFA is required to change bucket
    > versioning state

-   MFA is required to delete versions

![](media/image70.jpeg){width="6.25625in" height="2.2555555555555555in"}

**S3 Performance Optimization**

> When uploading to S3, and object is loaded as a single blob of data in
> a single stream

-   a file is uploaded and becomes an object via the **S3:PutObject
    > AP**I. **This happens a single stream**

-   **if a stream fails, the whole upload fails**, which needs a full
    > restart

-   the speed and reliability of the upload process is limited by the
    > limit of 1 stream of data

-   when transferring data between two points, the speed that the data
    > will transfer matches the lower speed from the two points

-   any upload with the **put** method, has a limit of maximum 5GB

> A solution for this is **multipart upload**

-   improves the speed and reliability of uploads to S3

-   it does its job by dividing the data into individual parts

    -   the minimum size of the original blob of data is 100 MB

    -   a blob can be split into maximum of 10,000 parts

        -   each part can range from 5MB to 5GB

        -   the last part is called a leftover, and can be smaller than
            > 5MB if needed

    -   each part can fail and be restarted in isolation

        -   the whole data transfer does not need to be restarted if a
            > part fails

    -   the transfer rate in this case is the speed of transfer of all
        > parts

> ![](media/image71.png){width="2.2125in"
> height="1.1423611111111112in"}**S3 Accelerated Transfer**

-   we do not have control of the path, that the transfer is made from
    > point A to point B (look like depends on internet transfer

> and the internet have multiple roots)

-   **transfer acceleration uses the network of AWS edge location**

![](media/image72.png){width="2.9685728346456695in"
height="1.774194006999125in"}

-   **S3 transfer acceleration** needs to be enabled, as by default is
    > switched off

    -   there are few constrains to enabled it

        -   the bucket name needs to not contain any periods

        -   needs to be DNS compatible in its naming

-   when the transfer acceleration is enabled, the data being uploaded
    > instead of going to the S3 directly it immediately enters the
    > **closest best performing AWS edge location**

-   from here the data is transferred through AWS network, a network
    > that is fully controlled by AWS - direct link

    -   the private AWS network is designed to link regions to other
        > regions

> [[s3-accelerate-speedtest.s3-accelerate.amazonaws.com/en/accelerate-speed-comparsion.html]{.underline}](http://s3-accelerate-speedtest.s3-accelerate.amazonaws.com/en/accelerate-speed-comparsion.html)

**Key Management Service (KMS)**

> **Key Management Service** is not part of S3, but is used in most AWS
> services **that use encryption**. and S3 uses encryption.
>
> **KMS** is a **regional and public service.** (is a separate product
> in each region)

-   it is public that you need permission to access it

-   allows you store, create and manage **cryptographic keys**

-   these keys are used to convert plain text to cipher text and
    > vice-versa

-   can handle symmetric and asymmetric keys

-   can perform cryptographic operations such as encryption and
    > decryption

> ![](media/image39.jpeg){width="0.16666666666666666in"
> height="0.14583333333333334in"}- **the keys never leave the
> product** - **provides FIPS 140-2 (Level 2 or 3)**

-   the keys are locked inside KMS service

-   its function is to secure and make sure that the keys never leave
    > the service

> Customer Master Key (CMK)
>
> The main thing that KMS manages is **CMS** (Customer master keys)

-   CMK are used by KMS for cryptographic operations

-   it can be used by entities, applications and AWS services

-   CMS are logical - a container for the actual physical master keys

-   It contains:

    -   a key ID - used as an identifier of the key

    -   creation date

    -   a key policy

    -   a description

    -   a state of the keys: active or inactive

-   can be generated or imported by KMS

> ![](media/image39.jpeg){width="0.16666666666666666in"
> height="0.14583333333333334in"}○ **can be used to encrypt or decrypt
> data up to 4KB**
>
> The process:

1.  After peaking a region a key can be created (a CMK)

2.  A CMK logical container is created which contains physical baking
    > key material

    a.  This is what KMS creates, stores and manages

    b.  the CMK are never stored in a persistent store if they are not
        > encrypted (KMS encrypts the key before storing it on the disk)

3.  Request to encrypt some data

    a.  this is achieved by making an encryption call, providing a key
        > and the data to be encrypted

4.  KMS accept the data and if the entity has permissions to use the CMK

    a.  the KMC decrypt the key

    b.  uses the decrypted key to encrypt the plain text data to cypher
        > text

KMS returns the data to the entity

1.  To decrypt the data, an entity needs to request the decrypt

2.  KMC does not need to be told which CMK to use to decrypt the data

> a\. that information is encoded into the cypher text of the data that
> needs to be decrypted

3.  KMS will decrypt the CMK

4.  Will use de decrypted CMS to decrypt the cypher text

5.  Will return the data to the entity

![](media/image73.png){width="7.009027777777778in"
height="3.942361111111111in"}

![](media/image74.png){width="7.009027777777778in"
height="3.942361111111111in"}

![](media/image75.jpeg){width="0.16666666666666666in"
height="0.16666666666666666in"}

> During both processes the **CMK does not leave the KMS, the decrypted
> CMK is not stored on the**
>
> **disk and at every step the entity needs permissions to perform this
> operations**

-   **EACH OPERATION NEEDS DIFFERENT PERMISSIONS**

    -   **Administrative permissions** - delete and create keys

    -   **Usage permissions** - encrypt and decrypt

![](media/image38.jpeg){width="0.16666666666666666in"
height="0.16666666666666666in"}

> **Role separation** is where different roles are given different
> access rights within a product.
>
> Data Encryption Keys (DEKs)
>
> DEKs are another type of key which KMS can generate using a CMK.

-   can be used to encrypt data larger than 4 KB

-   this is linked to a specific CMK

> ![](media/image39.jpeg){width="0.16666666666666666in"
> height="0.14583333333333334in"}- KMS does not store the DEK in any way

-   it provides it to the key to the service or entity that needs it and
    > then it discards it

> The process:

1.  When a data encryption key is generated KMS provides two versions of
    > that encryption key

    a.  plain text version

    b.  cypher text version

2.  Encrypt data with the plain text version key

    a.  once the encryption is done, the plain text key is
        > discarded(deleted)

3.  The encrypted key and the encrypted data are stored only

![](media/image75.jpeg){width="0.16666666666666666in"
height="0.16666666666666666in"}

> KMS does not perform the encryption or decryption on the data larger
> than 5 KB

-   the identity or the service using KMS does

> KMS does not track the usage of the data encryption keys

![](media/image38.jpeg){width="0.16666666666666666in"
height="0.16666666666666666in"}

> **S3 when using encryption, generates a data encryption key for every
> object!**

![](media/image76.png){width="6.647916666666666in"
height="3.7395833333333335in"}

> Key Concepts

1.  **CMKs** are isolated to a region and they never leave that region

2.  The never leave the **KMS** service. They cannot be extracted

3.  There are two types of CMKs:

    a.  **AWS managed CMKs**

        i.  created automatically by AWS when a service uses KMS
            > encryption

    b.  **Customer Manages CMKs**

        i.  are created explicitly by the customer

        ii. are much more configurable

> ![](media/image39.jpeg){width="0.16666666666666666in"
> height="0.14583333333333334in"} **c. both support key rotation**
>
> Rotation is the process when the physical backing material is changed

-   with **AWS Managed Keys** this cannot be disabled and is set to
    > rotate material every 1,095 days (3 years)

-   with **Customer Managed Keys** the rotation is optional and happens
    > once a year if its enabled

    -   CMK contains the current backing key and all the previous
        > backing keys used for backing material

    -   aliases are a shortcut to a particular CMK - are also per region

> Every **CMK has a customer policy**
>
> ![](media/image39.jpeg){width="0.16666666666666666in"
> height="0.14583333333333334in"}- **KMS has to be explicitly told they
> keys trust the AWS account they are in.**

-   the key trusts an account, so that the account can manage the keys

> ![](media/image77.png){width="6.457446412948381in"
> height="3.6324398512685914in"}![](media/image78.jpeg){width="0.16666666666666666in"
> height="0.14583333333333334in"}○ **IAM is trusted by the account, and
> the account needs to be trusted by the key**

![](media/image79.png){width="6.5in" height="3.254166666666667in"}[Let's
encrypt and decrypt the data with aws-cloud 9 or terminal using
AWS-KMS]{.mark}

![](media/image80.png){width="4.255813648293963in"
height="2.9771544181977254in"}

![](media/image81.png){width="3.032638888888889in"
height="1.895138888888889in"}

> **\# Generate Battleplans**

echo \"find all the doggos, distract them with the yumz\" \>
battleplans.txt

> **\# Encrypt**
>
> aws kms encrypt \\
>
> \--key-id alias/catrobot \\
>
> \--plaintext fileb://battleplans.txt \\
>
> \--output text \\
>
> \--query CiphertextBlob \\
>
> \--profile iamadmin-general \| base64 \\
>
> \--decode \> not_battleplans.enc
>
> **\# Decrypt**
>
> aws kms decrypt \\
>
> \--ciphertext-blob fileb://not_battleplans.enc \\ \--output text \\
>
> \--profile iamadmin-general \\
>
> \--query Plaintext \| base64 \--decode \> decryptedplans.txt

**S3 Encryption**

> **we do not define encryption at the bucket level**

-   we define encryption at the object level

    -   each object inside a bucket can use **different encryption
        > settings**

-   There are two main method of encryption:

    -   **client side encryption**

        -   the data is encrypted by the client, before they are
            > uploaded

        -   the data is cypher text the entire time in transit and on
            > the final destination

        -   the data cannot be seen in plain text at any given time

        -   **this type of encryption is the client responsibility:**

            -   generate a key

            -   store that key

            -   know what key belongs to what file

            -   encryption is done by the client before is uploaded to
                > S3

            -   S3 is used for storage **only**

    -   **server side encryption**

        -   the data is encrypted in transit using HTTPS, the object
            > themselves are not encrypted

        -   when it reaches the **S3 endpoint** is in plain text

        -   once the data hits **S3 is then encrypted** by the S3
            > infrastructure

        -   with this type of encryption you allow S3 to perform **some
            > or all those process**

    -   **both of them refer to encryption at REST** (when they are
        > stored on the disk)

-   encryption in standard comes by default with S3 service - data is
    > encrypted in transit

![](media/image82.png){width="2.560416666666667in"
height="1.7527777777777778in"}![](media/image83.jpeg){width="6.5256944444444445in"
height="3.152083333333333in"}

> Server side encryption
>
> There are 3 types of server side encryption:

1.  **SSE-C** (Server side encryption with customer provided keys)

    -   The customer is responsible to manage the encryption and
        > decryption keys

    -   The server manages the encryption/decryption process

> ![](media/image78.jpeg){width="0.16666666666666666in"
> height="0.14583333333333334in"}○ When using this service you are
> required to provide the **object** and the **key**
>
> When the key and the object arrive on the server, the object is
> encrypted using that key and store the object on the server with a
> hash of that key (the key is discarded after is hashed)
>
> ![](media/image75.jpeg){width="0.16666666666666666in"
> height="0.16666666666666666in"}○ The hash of the key is one way
> (cannot be used to get the key). It is used in the decryption process
> to check the authenticity of the key provided to decrypt the object

![](media/image84.jpeg){width="5.886111111111111in"
height="2.652083333333333in"}

2.  **SSE-S3** (Server side encryption with Amazon S3 managed keys)

    -   With this service, Aws manages the encryption and the decryption
        > process as well as the key **generation and management**

    -   In this case, the client provides just the data in plaintext

    -   AWS creates a **master key** to be used for the plaintext data
        > to be encrypted

-   Is handled end to end by AWS can cannot be configured

> ! each object will have a unique key

-   AWS generates a key for each object, and uses that key to encrypt
    > that object

-   the **master key** is used to encrypt the key of the object after
    > the object was encrypted

-   the un-encrypted version of that key is discarded, and the encrypted
    > key is stored with that encrypted object

![](media/image85.png){width="5.772916666666666in"
height="3.1590277777777778in"}

> **It does come with some disadvantages:**

-   **you cannot control the rotation of the key**

> ![](media/image75.jpeg){width="0.16666666666666666in"
> height="0.16666666666666666in"}^▪^ **you cannot use role separation**

-   **you cannot control or manage the keys, and you cannot control who
    > uses those key**

**\
**

2.  **SSE-KMS** (Server side encryption with customer master keys stored
    > in AWS key management service)

    -   is very much like SSE-S3 but it allows the KMS service to manage
        > the keys

    -   every object that is uploaded to a bucket requires a CMK

> **this CMK is used to generate one unique encryption key for every
> object that is encrypted using the SSE-KMS**

![](media/image86.png){width="6.60625in" height="3.7159722222222222in"}

This gives the option of not using the default CMK that S3 creates. You
can create and use a **customer managed CMK** that allows:

-   role separation

    -   \[S3 administrators - not being able to read the objects
        (decrypt the objects)\]

-   Key Policies

![](media/image87.png){width="6.60625in" height="4.075in"}

Summary

![](media/image88.jpeg){width="6.207638888888889in"
height="3.0805555555555557in"}

Default Bucker Encryption

> Using the **x-amz-server-side-encryption** header, objects are
> encrypted. Without the header, the objects will not use encryption.
>
> If you do spacify the
>
> **x-amz-server-side-encryption : AES256 (it used SSE-S3)**
>
> **x-amz-server-side-encryption : aws:kms (it used SSE-KMS)**

![](media/image89.png){width="6.60625in" height="3.7159722222222222in"}

**S3 Storage Classes**

> S3 Standard
>
> The default S3 storage class is called **S3 Standard**.
>
> When using S3 standard:

-   objects are saved in at least 3 availability zone

-   that means that S3 standard is able to cope to availability zone
    > failures

-   this level of replication means:

    -   11 nines of durability: for 10 million objects within an S3
        > bucket, on average you might lose an object every 10,000 years

    -   uses MD5 checksums with cyclic redundancy to detect and resolve
        > any data issues

-   when objects are stored successfully and durably, a **HTTP/1.1 200
    > ok** response is provided to the **S3 API**

> **Endpoint**

-   billing a **GB/month fee for data stored**, **a dollar/GB charge for
    > transfer OUT (IN is free)** and **a price per 1000/requests**

    -   **there is no specific retrieval fee, no minimum duration and no
        > minimum size**

-   access to S3 is instantly - has a milliseconds first byte latency
    > (data requested is available in milliseconds)

    -   objects can be made publicly available

> ![](media/image90.jpeg){width="0.16527777777777777in"
> height="0.14583333333333334in"}- **should be used for frequently
> accessed data**

![](media/image91.jpeg){width="6.861111111111111in"
height="3.410416666666667in"}

> S3 Standard Infrequent Access (S3 Standard-IA)
>
> Standard-IA shares most of the architecture and characteristics with
> S3 Standard.

-   data is replicated over at least three availability zone in the
    > region

    -   11 nines of durability: for 10 million objects within an S3
        > bucket, on average you might lose an object every 10,000 years

    -   uses MD5 checksums with cyclic redundancy to detect and resolve
        > any data issues

-   durability, availability, first byte latency and can be made
    > publicly available are the same as in S3 Standard

-   Costs are **cheaper** in S3 Standard:

    -   request charge and data transfer out has the same price

    -   GB/months is about half the price

    -   retrieval fee has a cost of GB for retrieval which is expensive
        > for frequent accessed data

    -   **this class is designed for infrequently accessed data**

```{=html}
<!-- -->
```
-   has a minimum duration charge of 30 days - objects can be stored for
    > less time, but the minimum billing pay applies anyway

-   has a minimum capacity charge of 128KB/object. So objects that are
    > smaller than this size, are billed for 128KB

> ![](media/image92.jpeg){width="0.16527777777777777in"
> height="0.16527777777777777in"}○ **this class is cost effective for
> data as long as the objects are not accessed frequently, as long as
> the data is not stored for short term and the objects stored are not
> tiny in size**

![](media/image93.jpeg){width="7.074305555555555in"
height="3.4743055555555555in"}

> S3 One Zone - Infrequent Access (S3 One Zone - IA)
>
> This class is similar to S3 Standard-IA in many ways.

-   it is cheaper than S3 standard and S3 Standard - IA

-   retrieval fee has a cost of GB for retrieval which is expensive for
    > frequent accessed data

-   has a minimum duration charge of 30 days - objects can be stored for
    > less time, but the minimum billing pay applies anyway

-   has a minimum capacity charge of 128KB/object. So objects that are
    > smaller than this size, are billed for 128KB

> ![](media/image94.jpeg){width="0.16527777777777777in"
> height="0.13541666666666666in"}- **data stored in this class is stored
> in only one availability zone**

-   **does not have the replication as the other two classes**

-   **less resilience**

-   **the durability is the same - 11 nines**

    -   11 nines of durability: for 10 million objects within an S3
        > bucket, on average you might lose an object every 10,000 years

        -   data is still replicated in that availability zone (multiple
            > copies of data exist) but if the zone fails the data is
            > lost

    -   uses MD5 checksums with cyclic redundancy to detect and resolve
        > any data issues

> ![](media/image95.jpeg){width="0.16527777777777777in"
> height="0.14583333333333334in"}- **should be used for long-lived data
> (as the size and duration minimums are in place)**

-   not frequent accessed data

-   not small objects in size (less then 128KB)

> ![](media/image95.jpeg){width="0.16527777777777777in"
> height="0.14583333333333334in"}- **should be used for data that is not
> critical! (data that can be easily replaced)**

![](media/image96.png){width="7.238888888888889in"
height="10.002083333333333in"}

S3 Glacier

> S3 Glacier has data replicated over at least three availability zone
> in the region.

-   this level of replication means:

    -   11 nines of durability: for 10 million objects within an S3
        > bucket, on average you might lose an object every 10,000 years

    -   uses MD5 checksums with cyclic redundancy to detect and resolve
        > any data issues

-   it is really cost-effective as it has a GB/month fee of about a
    > sixth(1/6) of the S3 Standard

-   objects stored in S3 Glacier are called **cold objects**

```{=html}
<!-- -->
```
-   ○ **not ready to be used - they are not immediately available**

    -   **to access them a retrieval process needs to be made**

    -   **when retrieved the objects are stored in S3 Standard - IA
        > temporarily** - they are removed after they are accessed

    -   every retrieval process is billed

        -   **Expedited** - data is available in 1 - 5 minutes (is the
            > most expensive)

        -   **Standard** - data is available in 3 - 5 hours

        -   **Bulk** - data is available in 5 - 12 hours (low cost)

        -   Faster = more expensive

        -   first-byte latency can be from minutes to hours

> ![](media/image94.jpeg){width="0.16527777777777777in"
> height="0.13541666666666666in"}○ **they cannot be made public**

-   has a 40KB minimum billing size

-   90 days minimum billing duration

> ![](media/image90.jpeg){width="0.16527777777777777in"
> height="0.14583333333333334in"}- **used when the object stored are for
> archives, where frequent or real time data isn\'t needed**

![](media/image97.png){width="6.94375in" height="10.002083333333333in"}

> S3 Glacier Deep Archive
>
> S3 Glacier Deep Archive has the price fourth (1/4) of the S3 Glacier.

-   has data been replicated over at least three availability zone in
    > the region.

    -   this level of replication means:

        -   11 nines of durability: for 10 million objects within an S3
            > bucket, on average you might lose an object every 10,000
            > years

        -   uses MD5 checksums with cyclic redundancy to detect and
            > resolve any data issues

-   objects stored in S3 Glacier are called **freeze objects**

    -   has a 40KB minimum billing size

    -   180 days minimum billing duration

-   objects cannot be made publicly available

-   access to the data requires a retrieval process

    -   **standard -** up to 12 hours

    -   **bulk -** up to 48 hours

    -   first bye latency = hours or days

> ![](media/image98.jpeg){width="0.16527777777777777in"
> height="0.14583333333333334in"}- **should be used for data which is
> archival, and which rarely (if ever) needs to be accessed**

![](media/image99.jpeg){width="6.8625in" height="3.3125in"}

> S3 Intelligent-Tiering
>
> Is different from all the other S3 classes
>
> It contains 5 different tiers of storage, there are a number of ways
> that an object can be stored:

-   frequent access tier (like S3 standard)

-   infrequent access tier (like S3 standard IA)

-   archive (Glacier)

-   deep archive (Glacier Deep Archive)

> ![](media/image100.jpeg){width="0.16527777777777777in"
> height="0.14583333333333334in"}- you do not have to worry about moving
> objects between tiers

-   the system does it for you

    -   the system monitors the usage of the object

> ![](media/image101.jpeg){width="0.16319444444444445in"
> height="0.16527777777777777in"}□ if an object is not used for 30 days
> it is moved to from frequent access tier to infrequent access tier
>
> ![](media/image101.jpeg){width="0.16319444444444445in"
> height="0.16527777777777777in"}□ if the object is used even less can
> be moved to the archive tiers, **but it is optional**

-   90 days for archive

-   180 days for deep archive

-   **for this two tires, the access to the objects is not instantly, it
    > is a**

> **retrieval time to access them**
>
> ![](media/image102.jpeg){width="0.16319444444444445in"
> height="0.16319444444444445in"}□ if an object is in the infrequent
> tier, and the system detects that it is used frequent again it is
> moved back to the frequent tier

-   Intelligent tiering has a monitoring and automation cost/1000
    > objects - instead of the retrieval cost

-   the cost of the tires are the same as the S3 storage classes

> ![](media/image92.jpeg){width="0.16527777777777777in"
> height="0.16527777777777777in"}- **it is ideal for long-lived data,
> because it has a 30 day minimum billing period, and is also ideal
> where the usage of objects is changing or is unknown**

-   **ideal for changing access frequency**

![](media/image103.png){width="7.189583333333333in"
height="4.044399606299213in"}

**S3 Lifecycle Configuration**

> Lifecycle rules can be created on S3 buckets which can automatically
> transition or expire objects in that bucket.

-   a great way to optimize costs

-   a configuration for S3 buckets is a set of rules which apply to a
    > particular bucket

    -   rules consists of actions

-   the rules can apply to a bucket or a set of objects defined by
    > prefixes or tags

-   there are two types of actions

> ![](media/image104.jpeg){width="0.16666666666666666in"
> height="0.13541666666666666in"}○ **transition** actions

-   which can change the storage class

> ![](media/image104.jpeg){width="0.16666666666666666in"
> height="0.13541666666666666in"}○ **expiration** actions

-   which can delete affected objects or versions of objects

-   automate the deletion of objects

![](media/image105.png){width="4.117361111111111in"
height="0.18680555555555556in"}

> ![](media/image75.jpeg){width="0.16666666666666666in"
> height="0.16666666666666666in"}- [these rules are not based on access
> -]{.mark} not moved according to their accessing intervals, they are
> moved [between classes or they are deleted based on hardcoded
> rules]{.mark}
>
> Transitions

-   lifecycle transitions are like a waterfall

    -   starting with S3 Standard, followed by S3 Infrequent Access, S3
        > Intelligent Tiering, S3 One zone IA, S3

> Glacier instant retrieval, Glacier Deep and S3 Glacier Deep Archive

-   ○ transition flows in a downward direction **only**

![](media/image106.png){width="7.189583333333333in"
height="4.044444444444444in"}

![](media/image107.png){width="7.189583333333333in"
height="4.044444444444444in"}

-   when transitioning **smaller objects** from S3 Standard to IA or
    > Intelligent Tiering because all of

> these have a minimum storage billing
>
> ![](media/image38.jpeg){width="0.16666666666666666in"
> height="0.16666666666666666in"}- to move objects automatically from S3
> standard to S3 Standard IA and S3 one Zone IA days, the objects
> **need** to be 30 days in S3 Standard
>
> ![](media/image38.jpeg){width="0.16666666666666666in"
> height="0.16666666666666666in"}- To transition objects from S3
> Standard IA, S3 One Zone IA, and S3 Intelligent Tiering to Glacier or
> Glacier Deep Archive, they object need to be in 30 days in the S3
> Standard IA, S3 One Zone IA, and S3 Intelligent Tiering
>
> ![](media/image108.jpeg){width="0.16666666666666666in"
> height="0.16666666666666666in"}- You can define two rules:

-   one rule to move an object from the Infrequent Access tier

-   second rule to move it from the Infrequent Access tier to Glacier

```{=html}
<!-- -->
```
-   **these two rules won\'t suffer the 30 days minimum**, but it will
    > be charged for the minimum

> duration billable duration

-   if a single rule is used **then you need to wait for the minim
    > period between transitions**

**S3 Replication**

> S3 replication is a feature that allows the configuration of
> replication of objects between a source and destination, S3 bucket.
>
> There are 3 types of replication supported by S3:

1.  Cross-Region Replication (CRR)

    -   allows the replication of objects from s source bucket to a
        > destination bucket in **different AWS regions**

    -   **needs versioning enabled**

2.  Same Region Replication (SRR)

    -   allows replication of objects from a source bucket to a
        > destination bucket in the **same region**

3\. different AWS accounts replication

> Architecture

-   **replication configuration is applied on the source bucket**

    -   the configuration states the replication from a source bucket to
        > a destination bucket

    -   the configuration states the following

        -   the destination bucked to be used for the replication
            > process

        -   an IAM role to use for the replication process

        -   The roles permission policy gives permission to read objects
            > on the source bucket and replicate those objects to the
            > destination bucket

        -   the replication is encrypted

    -   **same AWS account replication**

        -   in this scenario both buckets are owned by the same AWS
            > account

        -   they both trust the same IAM service and the IAM role

        -   the role automatically has access to both the source and the
            > destination buckets, and to the permission policy that
            > grants the access

    -   **different AWS accounts replication**

        -   the destination bucket because is in a different AWS
            > account, does **not trust** the other account or the role
            > that is used to replicate the bucket contents

        -   the role that is designed to perform the replication isn\'t
            > by default trusted by the destination AWS account

            -   a bucket polity is added on the destination bucket which
                > allows the role in the source account to replicate
                > objects into it

![](media/image109.jpeg){width="7.179166666666666in"
height="3.3979166666666667in"}

![](media/image110.png){width="7.381944444444445in"
height="10.011111111111111in"}

> Replication options

-   all objects or a subset of objects can be replicated

-   the store class of the destination bucket can be selected

    -   by default is use the same class as the source bucket

        -   for a backup a One Zone IA is good

-   ownership of the buckets

    -   by default the objects in the destination bucket are owned by
        > the source account

-   replication time control (RTC)

    -   S3 Replication Time Control is designed to replicate 99.99% of
        > objects within 15 minutes after upload, with the majority of
        > those new objects replicated in seconds. S3 RTC is backed by
        > an SLA with a commitment to replicate 99.9% of objects within
        > 15 minutes during any billing month.

> Considerations

1.  replication is not retroactive

    -   you enable replication with two buckets: a source and a
        > destination bucket

    -   only after the source and the destination bucket are named, are
        > objects replicated from

> source to destination
>
> ![](media/image38.jpeg){width="0.16666666666666666in"
> height="0.16666666666666666in"}○ [if you enable replication on a
> bucket that already has objects in it, the existing objects will not
> be replicated]{.mark}
>
> ![](media/image104.jpeg){width="0.16666666666666666in"
> height="0.13541666666666666in"}○ both the source and the destination
> bucket need to have versioning enabled

2.  it is a one-way replication

> ![](media/image104.jpeg){width="0.16666666666666666in"
> height="0.13541666666666666in"}○ from source to destination

-   if objects are added to the destination bucket, they will not be
    > added to the source bucket

3.  objects can be replicated:

    -   if they are unencrypted

    -   or they are encrypted with SSE-S3 or SS3-KMS

        -   cannot replicate objects using SSE-C - because it needs the
            > keys

4.  the source bucket owner needs permission on **all** objects that
    > will be replicated

    -   if changes are made in the source bucket by lifecycle
        > management, they will not be replicated in the destination
        > bucket

    -   only user events are replicated

5.  system events cannot be replicated

6.  glacier and glacier-deep archive objects cannot be replicated

7.  deletes are not replicated

> Why use replications?

1.  for same region replication (SRR)

    a.  log aggregation - merge multiple logs

    b.  synchronize production and test accounts

    c.  resilience with strict sovereignty requirements

2.  for cross-region replication (CRR)

    a.  global resilience improvements

        i.  backups of data copied in different AWS regions to cope with
            > large-scale failure

    b.  reduce latency

        i.  for better performance

**S3 Presigned URLs**

> **Presigned URLs** are the way of giving another entity, or
> application access to an object inside an S3 bucket, using **your
> credentials** in a **safe and secure way.**

-   an S3 bucket that does not have any public access configured - its
    > state is in a private configuration

    -   this means, that an entity needs to access the bucket or its
        > objects need to authenticate and have permission to do so

-   we can allow access to objects within a bucket or buckets to an
    > unauthenticated entity in three different ways

1.  give the entity an AWS identity

2.  give the entity some AWS credentials

3.  make the bucket or the objects public

4.  presigned URLs

    -   the **iamadmin** user make a request to S3 to generate a
        > presigned URL

        -   the iamadmin user needs to provide his credentials

        -   the bucket name

        -   an object key

![](media/image111.png){width="0.6444444444444445in"
height="0.8972222222222223in"}

> □ expiry date and time

-   specify how the objects will be accessed

```{=html}
<!-- -->
```
-   the S3 creates a presigned URL and returns it to iamadmin

    -   the URL has encoded inside it the details that the **IAMadmin**
        > provided

-   the URL can be passed to the mystery identity

    -   the identity can use the URL to access the specific S3 bucket or
        > objects

        -   until the URL expires

    -   the mystery identity that uses the URL interacts with the S3 as
        > the person who generated it

-   the URL can be used to GET (download) or to PUT (upload)

![](media/image112.png){width="7.550694444444445in"
height="4.247222222222222in"}

> Example
>
> We have an application server in the cloud, which hosts the
> application. This is a video-processing application. Large video files
> had been migrated from the application server to a media S3 bucket.
>
> Previously the videos were hosted on the application server and it
> could control access to the video files. Hosted in the S3 bucket,
> either every user needs an AWS identity to access the videos, or the
> videos need to be public. Neither is a good solution. However, we can
> use the pre-signed URLs, to keep the bucket private and create an IAM
> user for this application.

1.  when an application user interacts with the web application it makes
    > a request

2.  the request is for a page that has a video associated with it

3.  the app running on the server knows that it can directly return the
    > information that is requested, but the video it is hosted on a
    > private S3 bucket

4.  therefore, the application initiates a request to S3 asking to
    > generate a presigned URL for that particular video associated with
    > the web request

5.  the S3 services create an URL that has encoded within the
    > authenticated information for that IAM user, to access the video
    > on a short time basis (for 2 to 3 hours)

6.  the S3 service returns the URL to the server application, and the
    > server application returns the response including the video to the
    > end user

7.  the web application running on the user device uses the pre-signed
    > URL to securely access the particular object (the requested video)

![](media/image113.png){width="7.584027777777778in"
height="10.002083333333333in"}

> S3 presigned URLs are used when buckets are private for different
> reasons and the access needs to be controlled.
>
> **Presigned URLs are used to access objects within a private S3
> bucket, with the access rights of the entity that generates them. The
> URLs are time-limited and they encode all of the authentication
> information needed inside. They can be used to upload or download
> objects.**
>
> Exam power UP

![](media/image114.jpeg){width="0.14166666666666666in"
height="0.14166666666666666in"}

> **1. you can create a URL for an object you DO NOT have access to**

-   **the generated URL will also have no access to that object**

```{=html}
<!-- -->
```
-   **matches the identity that generated that URL**

-   **matches the permissions that the identity that generated the URL
    > has at the time when the mystery identity accessed the**

> **URL**

-   **cannot generate presigned URLs for non-existing objects**

![](media/image114.jpeg){width="0.14166666666666666in"
height="0.14166666666666666in"}

> **3. DO NOT GENERATE presigned URLs with a role, as the URL stops
> working when temporary credentials expire**
>
> Commands to create a presigned URL through the command line from the
> console
>
> aws s3 ls
>
> aws s3 presign objectURI \--expires-in 180 // 180 is in seconds
>
> ![](media/image115.png){width="5.159095581802275in"
> height="2.902083333333333in"}

**S3 Select and Glacier Select**

> S3 Select and Glacier Select are ways to retrieve parts of objects,
> rather than a whole object.

-   s3 can store an infinite number of objects, each object with a
    > maximum size of 5TB

    -   if we retrieve a whole 5TB object we consume time and 5TB of
        > transfer

    -   this can be filtered on the client side, but the resources had
        > been consumed

-   S3 and the Glacier allow the partial download of an object

    -   can be obtained with SQL like the statement

        -   this is a filter on the S3 service

    -   allows you to operate in a number of file formats such as CSV,
        > JSON, Parquet, VZIP2 compression for CSV and JSON

![](media/image116.jpeg){width="7.032638888888889in"
height="3.2958333333333334in"}

**[Cross Origin Resource Sharing (CORS)]{.mark}**

+----------------------------------------------+-----------------------+
| Friday, July 9, 2021                         | > 3:00 PM             |
+==============================================+=======================+
+----------------------------------------------+-----------------------+

-   When we open the browser on a device and open a web app such as
    > **catagram.io**, then catagram.io is the origin

    -   the website is stored in a bucket

    -   in this case the browser makes some web calls to catagram.io

        -   get index.html

        -   get serverless.js

        -   get catagram.png

    -   the request get returned without any security issues

        -   called same origin request

        -   the browsers requests the index.html. which has references
            > to serveless.js and catagram.png

            -   all are on the same domain, same origin

    -   to load the application, other additional requests

        -   an API call is made to an API gateway to get additional
            > application information and pull some images that the
            > users of the application has access to

        -   based on the API response, an image is loaded from another
            > bucket

            -   there are known as cross-origin requests because they
                > are made to different domains from different origins

            -   **by default, cross-origin request are normally
                > restricted** and this can be changed with CORS
                > configuration

    -   **CORS** configuration are defined on the other origins

        -   if configured they will allow these cross-origin requests

        -   they allow from where requests are **allowed**

![](media/image117.jpeg){width="7.057638888888889in" height="3.5125in"}

> CORS configuration is made in JSON
>
> AWS Developer Page 71

![](media/image118.png){width="3.347916666666667in"
height="10.002083333333333in"}

> There are two different type of requests that can be made, and that
> require CORS configuration

1.  Simple requests

    -   directly access a different origin using a cross-origin request

    -   as long as the other origin is configured to allow request from
        > the original origin then it is accepted

2.  Preflight requests

    -   requires a check (known as preflight) which is done in advance
        > to the other origin

    -   the browser first sends a HTPP request to the other origin that
        > determinates if the request made is safe to send

> Components of CORS Configuration

1.  Access Control Allow Origin

    -   will contain

        -   a start (\*) allowing any origin to make requests

        -   a particular origin to make requests

2.  Access Control Max Age

    -   determinates how long preflight requests can be cashed

        -   how long the origin can communicate with the other origin,
            > until another preflight request needs to be made

3.  Access Control Allow Methods

    -   contains a wild card or a list of methods that can be used for
        > cross-origin requests

    -   GET, PUT or DELETE

4.  Access Control Allow Headers

    -   can be contained in a CORS configuration and within the response
        > to a preflight request

    -   used to indicate witch HTPP headers can be used with the actual
        > request

AWS Developer Page 72

**S3 Events**

> S3 Events allows the creation of event notification configuration on a
> bucket.

-   when enabled notification is generated when a certain thing occurs
    > within an S3 bucket

    -   these can be delivered to different destinations (SNS, SQS, and
        > Lambda Functions)

    -   this way you can event-driven processes which occur as a result
        > of different things happening within S3

-   various types of events are supported:

    -   when objects are created (by PUT, POST, COPY, and multi-part
        > upload operations is completed)

    -   on object deletion (Delete an object, or when a Delete marker is
        > created)

    -   restore actions (from Glacier (post initiated, or completed))

    -   replication (when an object is no longer tracked, operations are
        > missed, operations failed, etc)

> Process

1.  create a bucket

2.  create an event notification configuration

3.  when events occur and are stipulated in the notification
    > configuration, notifications are sent to the configured
    > destination

    -   events are generated by the S3 service (S3 principle)

    -   we need to add resource policies on each destination service -
        > allowing the S3 service to interact with them

    -   the events themselves are JSON objects

![](media/image119.jpeg){width="7.039583333333334in"
height="3.6222222222222222in"}

> EventBridge
>
> EventBridge is an alternative service, that supports more types of
> events and more services that notifications.

**S3 Access Logs**

> S3 Access Logs is a feature available in S3 that provides detailed
> records for the requests that are made to an Amazon
>
> S3 bucket.

-   a **source bucket** is a bucket that generated records

-   a **destination bucket** is where the records are stored

-   it is managed by a system known as the **S3 log delivery group**
    > which reads the logging configuration which is set to the source
    > bucket

-   enabling or changing the configuration to this service needs a few
    > hours to take effect

-   logs are delivered as log files and each file consists of a number
    > of log records and these are **newline-delimited**

-   each record consists of attributes such as:

    -   date and time of the event

    -   the requester

    -   the operation

    -   status codes

    -   error codes

    -   etc.

-   attributes within a record are **space-delimited**

-   **a single target bucket** can be used for many **source buckets -**

    -   the records can be separated easily using prefixes

    -   this is configured in the logging configuration that is set on
        > the **source bucket**

![](media/image120.jpeg){width="5.50625in"
height="2.5659722222222223in"}

**[S3 Requester Pays]{.mark}**

+----------------------------------------------+-----------------------+
| Friday, July 9, 2021                         | > 4:29 PM             |
+==============================================+=======================+
+----------------------------------------------+-----------------------+

> With Requester Pays buckets, the requester instead of the bucket owner
> pays the cost of the request and the data download from the bucket.
> The bucket owner always pays the cost of storing data. \... The
> request authentication enables Amazon S3 to identify and charge the
> requester for their use of the Requester Pays bucket.

-   S3 buckets charge for GB stored in a bucket

-   IN transfer are free

-   OUT transfers are charged

-   with **requester pay bucket**

> ![](media/image104.jpeg){width="0.16666666666666666in"
> height="0.13541666666666666in"}○ this a bucket setting

-   cannot be used the bucket as a static website hosting or BitTorrent

> ![](media/image39.jpeg){width="0.16666666666666666in"
> height="0.14583333333333334in"}○ **only authenticated identities** can
> use the bucket
>
> ![](media/image39.jpeg){width="0.16666666666666666in"
> height="0.14583333333333334in"}○ any session downloading data from a
> **requester pay bucket is paid by the consumer**

-   **these users need to supply the x-amz-request-payer header to
    > CONFIRM the payment responsibility**

![](media/image121.jpeg){width="7.167361111111111in"
height="3.5076388888888888in"}

**S3 Object Lock**

> Amazon S3 Object Lock is an Amazon S3 feature that allows you to store
> objects using a write once, read many (WORM) model. You can use WORM
> protection for scenarios where it is imperative that data is not
> changed or deleted after it has been written.

-   can be enabled on **new** S3 buckets

    -   for existing buckets, AWS support needs to be contacted

-   when enabled the versioning setting on the bucket needs to be
    > enabled too

-   cannot be disabled, or the versioning cannot be suspended

-   write-once-read-many (WORM) architecture

    -   object versions cannot be overwritten or deleted

-   **requires versioning and individual versions of objects are
    > locked**

-   an object version can have

1.  **S3 object lock retention period**

2.  **S3 object lock legal hold**

-   an object can have, both, one or none

-   can be defined on individual object versions or for all object
    > within a bucket

> Retention Period

-   when used you specify a retention period of day - years

> **1. Compliance mode**

-   it means that an object version cannot be deleted or overwritten for
    > the duration of the retention period

-   the retention period itself cannot be reduced and the retention mode
    > cannot be adjusted during the retention period

-   **no changes at all to all object version or retention period
    > settings (this includes the root user)**

![](media/image122.png){width="6.664583333333334in"
height="1.3034722222222221in"}

2.  **Governance Mode**

    -   while active the object version cannot be deleted or changed in
        > anyway

    -   you can grant special permissions to allow this to be changed

    -   certain identities can change settings and object version

        -   permission is required: **s3:BypassGouvernanceRetantion**

        -   header is requested:
            > **x-amz-bypass-governance-retention:true**

> ![](media/image123.jpeg){width="0.15138888888888888in"
> height="0.125in"}○ is very useful for:

-   accidental deletion

-   process reasons or governance reasons to keep object versions

-   to test settings before using the compliance mode

![](media/image124.jpeg){width="6.674305555555556in"
height="1.4354166666666666in"}

3.  **Legal hold**

    -   with this type there is no retention period set at all

    -   is used to set on an object version to be **ON** or **OFF**

    -   does not allow deletion or changing of object version

    -   to add or remove the legal hold the **s3:PutObjectLegalHold** is
        > required
        > ![](media/image125.jpeg){width="0.15138888888888888in"
        > height="0.125in"}○ used to:

> AWS Developer Page 76

-   prevent accidental deletions of object versions

-   when specific object versions need to be flagged

![](media/image126.png){width="7.148611111111111in"
height="10.002083333333333in"}

> THEY CAN NOT BE COMBINED

**Networking**

> Whenever you use a Cloud system, is done via networking.
>
> **OSI 7-Layer Model**
>
> ![](media/image127.png){width="7.675694444444445in"
> height="4.317361111111111in"}

**Host Layers**

• **How data is chopped off and reassembled, and how is formatted so
that is understandable by both sides of the network connection**

> **Media Layers**
>
> • **How date is moved from point A to point B**

**Layer 1 - Physical Layer**

> **Physical layer** is the networking **card**.
>
> The connection between cards is called a **physical medium** which is
> usually a copper cable, optical fiber or WIFI.
>
> For Copper cable, voltage is used to transmit data, using a low
> voltage as 0, and a high voltage as 1.

![](media/image128.jpeg){width="7.070833333333334in"
height="3.4743055555555555in"}

> If more devices need to communicate, a **hub** is needed. A **hub**
> job is to transmit to every device, what is receiving from a device.
> Anything received on any port, is transmitted to all the other ports!
>
> In this layer, none of the connected device has addressing
> (identities - names).
>
> Two devices might transmit at the same time, fact that might results
> into a collision - only one device can transmit at a time, so that the
> information transmitted can be read by the other devices.
>
> This layer has no media control access, or any collision detection,
> therefore, is a network is created using only layer 1, collision will
> be present.

![](media/image129.png){width="7.120138888888889in"
height="3.390277777777778in"}

**Layer 2 - Data Link Layer**

> The Data Link layer runs over the physical layer.
>
> The Data Link layer uses frames to send information between devices.
> Devices using this layer has a unique hardware address called a **MAC
> address**, which is represented by hexadecimal values.
>
> This address is not based on any software, it is uniquely attached to
> a piece of hardware.
>
> The MAC address is made into two parts:

1.  The OUI -- an organizationally unique identifier

2.  The NIC - network interface controller

> As the data link layer is based on layer one, the information is
> shared by layer 1. For simplicity, layer 2 transmits a frame, via
> layer 1, even layer 1 does not understands what it is sharing.
>
> ![](media/image130.jpeg){width="7.142361111111111in"
> height="3.435416666666667in"}Layer 2 brings identifiable devices,
> senders, and receivers to life.

![](media/image131.png){width="6.990277777777778in"
height="3.4972222222222222in"}

![](media/image132.png){width="7.384027777777778in"
height="3.5722222222222224in"}

![](media/image133.png){width="7.473611111111111in"
height="10.002083333333333in"}

> The data is **encapsulated** into the frame when transmitted, and
> extracted when it reaches the receiver.

![](media/image134.png){width="7.375in" height="10.002083333333333in"}

Collision detection

> A **switch** is a layer two hub, that understands frames.

![](media/image135.jpeg){width="7.269444444444445in"
height="3.495833333333333in"}

![](media/image136.png){width="7.4018689851268595in"
height="4.163740157480315in"}

![](media/image137.png){width="7.457638888888889in"
height="4.194444444444445in"}

**Layer 3 - Network Layer**

+---+-----+--------------------------+-----------------------------------+
| T |     | > 2:42 PM                |                                   |
| u |     |                          |                                   |
| e |     |                          |                                   |
| s |     |                          |                                   |
| d |     |                          |                                   |
| a |     |                          |                                   |
| y |     |                          |                                   |
| , |     |                          |                                   |
| J |     |                          |                                   |
| u |     |                          |                                   |
| n |     |                          |                                   |
| e |     |                          |                                   |
| 8 |     |                          |                                   |
| , |     |                          |                                   |
| 2 |     |                          |                                   |
| 0 |     |                          |                                   |
| 2 |     |                          |                                   |
| 1 |     |                          |                                   |
+===+=====+==========================+===================================+
|   | >   |                          |                                   |
|   |  Et |                          |                                   |
|   | her |                          |                                   |
|   | net |                          |                                   |
|   | >   |                          |                                   |
|   |  is |                          |                                   |
|   | >   |                          |                                   |
|   | the |                          |                                   |
|   | > m |                          |                                   |
|   | ost |                          |                                   |
|   | > p |                          |                                   |
|   | opu |                          |                                   |
|   | lar |                          |                                   |
|   | >   |                          |                                   |
|   |  la |                          |                                   |
|   | yer |                          |                                   |
|   | > 2 |                          |                                   |
|   | >   |                          |                                   |
|   |  co |                          |                                   |
|   | nne |                          |                                   |
|   | cti |                          |                                   |
|   | on. |                          |                                   |
+---+-----+--------------------------+-----------------------------------+
|   | >   |                          |                                   |
|   |  La |                          |                                   |
|   | yer |                          |                                   |
|   | > 3 |                          |                                   |
|   | >   |                          |                                   |
|   |  is |                          |                                   |
|   | >   |                          |                                   |
|   | the |                          |                                   |
|   | >   |                          |                                   |
|   | com |                          |                                   |
|   | mon |                          |                                   |
|   | >   |                          |                                   |
|   |  pr |                          |                                   |
|   | oto |                          |                                   |
|   | col |                          |                                   |
|   | >   |                          |                                   |
|   |  wh |                          |                                   |
|   | ich |                          |                                   |
|   | >   |                          |                                   |
|   | can |                          |                                   |
|   | > s |                          |                                   |
|   | pam |                          |                                   |
|   | >   |                          |                                   |
|   |  mu |                          |                                   |
|   | lti |                          |                                   |
|   | ple |                          |                                   |
|   | >   |                          |                                   |
|   | dif |                          |                                   |
|   | fer |                          |                                   |
|   | ent |                          |                                   |
|   | >   |                          |                                   |
|   |  La |                          |                                   |
|   | yer |                          |                                   |
|   | > 2 |                          |                                   |
|   | >   |                          |                                   |
|   | net |                          |                                   |
|   | wor |                          |                                   |
|   | ks. |                          |                                   |
+---+-----+--------------------------+-----------------------------------+
|   | >   |                          |                                   |
|   |  IP |                          |                                   |
|   | > a |                          |                                   |
|   | ddr |                          |                                   |
|   | ess |                          |                                   |
|   | >   |                          |                                   |
|   |  co |                          |                                   |
|   | mes |                          |                                   |
|   | > w |                          |                                   |
|   | ith |                          |                                   |
|   | >   |                          |                                   |
|   |  La |                          |                                   |
|   | yer |                          |                                   |
|   | >   |                          |                                   |
|   |  3. |                          |                                   |
+---+-----+--------------------------+-----------------------------------+
|   | >   |                          |                                   |
|   |  ** |                          |                                   |
|   | Rou |                          |                                   |
|   | ter |                          |                                   |
|   | s** |                          |                                   |
|   | >   |                          |                                   |
|   | are |                          |                                   |
|   | >   |                          |                                   |
|   |  la |                          |                                   |
|   | yer |                          |                                   |
|   | > 3 |                          |                                   |
|   | > d |                          |                                   |
|   | evi |                          |                                   |
|   | ces |                          |                                   |
|   | >   |                          |                                   |
|   |  wh |                          |                                   |
|   | ich |                          |                                   |
|   | > m |                          |                                   |
|   | ove |                          |                                   |
|   | > p |                          |                                   |
|   | ack |                          |                                   |
|   | ets |                          |                                   |
|   | >   |                          |                                   |
|   |  of |                          |                                   |
|   | > d |                          |                                   |
|   | ata |                          |                                   |
|   | >   |                          |                                   |
|   | acr |                          |                                   |
|   | oss |                          |                                   |
|   | >   |                          |                                   |
|   | dif |                          |                                   |
|   | fer |                          |                                   |
|   | ent |                          |                                   |
|   | >   |                          |                                   |
|   | net |                          |                                   |
|   | wor |                          |                                   |
|   | ks. |                          |                                   |
+---+-----+--------------------------+-----------------------------------+
|   | > * |                          |                                   |
|   | *Pa |                          |                                   |
|   | cke |                          |                                   |
|   | ts* |                          |                                   |
|   | * - |                          |                                   |
|   | > d |                          |                                   |
|   | ata |                          |                                   |
|   | > u |                          |                                   |
|   | nit |                          |                                   |
|   | > u |                          |                                   |
|   | sed |                          |                                   |
|   | >   |                          |                                   |
|   |  by |                          |                                   |
|   | >   |                          |                                   |
|   | the |                          |                                   |
|   | >   |                          |                                   |
|   |  la |                          |                                   |
|   | yer |                          |                                   |
|   | > 3 |                          |                                   |
|   | >   |                          |                                   |
|   | pro |                          |                                   |
|   | toc |                          |                                   |
|   | ol. |                          |                                   |
+---+-----+--------------------------+-----------------------------------+
|   | >   |                          |                                   |
|   |  \- |                          |                                   |
|   | >   |                          |                                   |
|   | are |                          |                                   |
|   | > v |                          |                                   |
|   | ery |                          |                                   |
|   | > s |                          |                                   |
|   | imi |                          |                                   |
|   | lar |                          |                                   |
|   | >   |                          |                                   |
|   |  to |                          |                                   |
|   | >   |                          |                                   |
|   | fra |                          |                                   |
|   | mes |                          |                                   |
+---+-----+--------------------------+-----------------------------------+
|   | > ○ |                          |                                   |
|   | >   |                          |                                   |
|   | wit |                          |                                   |
|   | hin |                          |                                   |
|   | >   |                          |                                   |
|   | fra |                          |                                   |
|   | mes |                          |                                   |
|   | >   |                          |                                   |
|   | the |                          |                                   |
|   | >   |                          |                                   |
|   | sou |                          |                                   |
|   | rce |                          |                                   |
|   | >   |                          |                                   |
|   | and |                          |                                   |
|   | >   |                          |                                   |
|   | the |                          |                                   |
|   | >   |                          |                                   |
|   |  de |                          |                                   |
|   | sti |                          |                                   |
|   | nat |                          |                                   |
|   | ion |                          |                                   |
|   | >   |                          |                                   |
|   | are |                          |                                   |
|   | >   |                          |                                   |
|   |  lo |                          |                                   |
|   | cal |                          |                                   |
+---+-----+--------------------------+-----------------------------------+
|   | > ○ |                          |                                   |
|   | > w |                          |                                   |
|   | ith |                          |                                   |
|   | >   |                          |                                   |
|   |  pa |                          |                                   |
|   | cke |                          |                                   |
|   | ts, |                          |                                   |
|   | >   |                          |                                   |
|   | the |                          |                                   |
|   | >   |                          |                                   |
|   |  de |                          |                                   |
|   | sti |                          |                                   |
|   | nat |                          |                                   |
|   | ion |                          |                                   |
|   | >   |                          |                                   |
|   | and |                          |                                   |
|   | >   |                          |                                   |
|   | sou |                          |                                   |
|   | rce |                          |                                   |
|   | >   |                          |                                   |
|   |  co |                          |                                   |
|   | uld |                          |                                   |
|   | >   |                          |                                   |
|   |  be |                          |                                   |
|   | >   |                          |                                   |
|   |  on |                          |                                   |
|   | >   |                          |                                   |
|   | dif |                          |                                   |
|   | fer |                          |                                   |
|   | ent |                          |                                   |
|   | >   |                          |                                   |
|   |  si |                          |                                   |
|   | des |                          |                                   |
|   | >   |                          |                                   |
|   |  of |                          |                                   |
|   | >   |                          |                                   |
|   | the |                          |                                   |
|   | >   |                          |                                   |
|   | pla |                          |                                   |
|   | net |                          |                                   |
+---+-----+--------------------------+-----------------------------------+
|   | >   |                          |                                   |
|   |  \- |                          |                                   |
|   | > p |                          |                                   |
|   | ack |                          |                                   |
|   | ets |                          |                                   |
|   | >   |                          |                                   |
|   |  ne |                          |                                   |
|   | ver |                          |                                   |
|   | >   |                          |                                   |
|   | cha |                          |                                   |
|   | nge |                          |                                   |
|   | > w |                          |                                   |
|   | hen |                          |                                   |
|   | > t |                          |                                   |
|   | ran |                          |                                   |
|   | sit |                          |                                   |
|   | ion |                          |                                   |
|   | ing |                          |                                   |
|   | > f |                          |                                   |
|   | rom |                          |                                   |
|   | >   |                          |                                   |
|   | sou |                          |                                   |
|   | rce |                          |                                   |
|   | >   |                          |                                   |
|   |  to |                          |                                   |
|   | >   |                          |                                   |
|   |  de |                          |                                   |
|   | sti |                          |                                   |
|   | nat |                          |                                   |
|   | ion |                          |                                   |
+---+-----+--------------------------+-----------------------------------+
|   | > ○ |                          |                                   |
|   | >   |                          |                                   |
|   | the |                          |                                   |
|   | >   |                          |                                   |
|   | fra |                          |                                   |
|   | mes |                          |                                   |
|   | >   |                          |                                   |
|   | are |                          |                                   |
|   | > c |                          |                                   |
|   | han |                          |                                   |
|   | ged |                          |                                   |
|   | >   |                          |                                   |
|   |  as |                          |                                   |
|   | >   |                          |                                   |
|   | the |                          |                                   |
|   | > p |                          |                                   |
|   | ack |                          |                                   |
|   | ets |                          |                                   |
|   | >   |                          |                                   |
|   |  go |                          |                                   |
|   | > f |                          |                                   |
|   | rom |                          |                                   |
|   | >   |                          |                                   |
|   | one |                          |                                   |
|   | >   |                          |                                   |
|   |  lo |                          |                                   |
|   | cal |                          |                                   |
|   | > n |                          |                                   |
|   | etw |                          |                                   |
|   | ork |                          |                                   |
|   | >   |                          |                                   |
|   |  to |                          |                                   |
|   | > a |                          |                                   |
|   | not |                          |                                   |
|   | her |                          |                                   |
+---+-----+--------------------------+-----------------------------------+
|   | > ○ |                          |                                   |
|   | >   |                          |                                   |
|   | the |                          |                                   |
|   | > p |                          |                                   |
|   | ack |                          |                                   |
|   | ets |                          |                                   |
|   | >   |                          |                                   |
|   | are |                          |                                   |
|   | >   |                          |                                   |
|   |  en |                          |                                   |
|   | cap |                          |                                   |
|   | sul |                          |                                   |
|   | ate |                          |                                   |
|   | >   |                          |                                   |
|   |  in |                          |                                   |
|   | >   |                          |                                   |
|   | the |                          |                                   |
|   | >   |                          |                                   |
|   |  fr |                          |                                   |
|   | ame |                          |                                   |
+---+-----+--------------------------+-----------------------------------+
|   | > * |                          |                                   |
|   | *IP |                          |                                   |
|   | >   |                          |                                   |
|   |  ad |                          |                                   |
|   | dre |                          |                                   |
|   | sse |                          |                                   |
|   | s** |                          |                                   |
+---+-----+--------------------------+-----------------------------------+
|   |     |                          |                                   |
+---+-----+--------------------------+-----------------------------------+
|   | >   |                          | > **version 6**                   |
|   | **v |                          |                                   |
|   | ers |                          |                                   |
|   | ion |                          |                                   |
|   | >   |                          |                                   |
|   | 4** |                          |                                   |
+---+-----+--------------------------+-----------------------------------+
|   |     |                          |                                   |
+---+-----+--------------------------+-----------------------------------+
|   | > • |                          | > • destination IP                |
|   | >   |                          |                                   |
|   |  de |                          |                                   |
|   | sti |                          |                                   |
|   | nat |                          |                                   |
|   | ion |                          |                                   |
|   | >   |                          |                                   |
|   |  IP |                          |                                   |
+---+-----+--------------------------+-----------------------------------+
|   | > • |                          | > • source IP                     |
|   | >   |                          |                                   |
|   | sou |                          |                                   |
|   | rce |                          |                                   |
|   | >   |                          |                                   |
|   |  IP |                          |                                   |
+---+-----+--------------------------+-----------------------------------+
|   | > • |                          | > • data                          |
|   | > p |                          |                                   |
|   | rot |                          |                                   |
|   | oco |                          |                                   |
|   | l - |                          |                                   |
|   | >   |                          |                                   |
|   |  wh |                          |                                   |
|   | ich |                          |                                   |
|   | >   |                          |                                   |
|   |  pr |                          |                                   |
|   | oto |                          |                                   |
|   | col |                          |                                   |
|   | >   |                          |                                   |
|   |  is |                          |                                   |
|   | > u |                          |                                   |
|   | sed |                          |                                   |
+---+-----+--------------------------+-----------------------------------+
|   | > • |                          | > • hop limit (time to live)      |
|   | >   |                          |                                   |
|   |  IC |                          |                                   |
|   | MP, |                          |                                   |
|   | > T |                          |                                   |
|   | CP, |                          |                                   |
|   | >   |                          |                                   |
|   | UDP |                          |                                   |
+---+-----+--------------------------+-----------------------------------+

![](media/image138.png){width="7.809722222222222in"
height="6.2555555555555555in"}

-   data

-   time to live (TTL) - if the packets cannot reach its destination,
    > this number declares how many hops the packet can take (so that it
    > won\'t travel forever) before being discarded

+---------------------------+------------------------------------------+
| • **Total number of IP    | > • **Total number of IP addresses       |
| addresses available:      | > available:                             |
| 4,294,967,296**           | > 340,282,366,                           |
|                           | 920,938,463,463,370,607,431,770,000...** |
+===========================+==========================================+
+---------------------------+------------------------------------------+

> •
>
> AWS Developer Page 85

![](media/image139.png){width="7.893055555555556in"
height="10.002083333333333in"}

First two digits - **network**

Last two digits - **host**

**Subnet masks allows a host to determine if an IP address is local or
remote. The result allows the sender to know if it needs a gateway
(router) or it can communicate locally.**

**255.255.0.0 -\> 11111111.11111111.00000000.00000000 /16 (ones)**

**everything with ones represents the network**

**everything with zeros represents the host**

**All data generated by your router is by default sent through the
internet service provider.**

**The internet provider has multiple interfaces route table to forward
the data**

1.  **each router has multiple route tables - a collection of routes**

2.  **every packet that arrives to the internet provider will check its
    > destination, and if a match is found the data is sent to the next
    > hop according to its destination**

> **0.0.0.0/0 - default route**

3.  **each time a hop is made, the frame where the packet is
    > encapsulated is changed, according to the new destination**

**Address Resolution Protocol (ARP)**

> AWS Developer Page 86

![](media/image140.png){width="7.893055555555556in"
height="10.002083333333333in"}

**ARP** is responsible of finding the **MAC** address of the
destination/next hop **host.**

![](media/image141.jpeg){width="3.8625in" height="1.863888888888889in"}

1.  **If routers receive packets within a frame that are not for them,
    > they are checking the routing table, match the next hop and create
    > a new frame for the packet, before it sends the frame to a new
    > router**

2.  **However, if a host receives a frame that is not destinated for it,
    > it drops the frame and packet.**

```{=html}
<!-- -->
```
1.  **Layer 3 has:**

    a.  **routes - where to send the packet**

    b.  **route tables**

    c.  **ARP - find the mac address for a certain IP**

    d.  **IP addresses**

    e.  can deliver packets out of order (wrong order)

![](media/image142.png){width="7.804861111111111in"
height="2.1347222222222224in"}

> AWS Developer Page 87

**Layer 4 - Transport Layer**

+--------------------------------------------------+-------------------+
| Wednesday, June 9, 2021                          | > 1:36 PM         |
+==================================================+===================+
+--------------------------------------------------+-------------------+

![](media/image143.png){width="7.589583333333334in"
height="7.276388888888889in"}

> **Layer 4 runs over Layer 3, therefore it needs IP addresses.**

-   **TCP -** has a reliable connection

-   **UDP -** is al about performance

> **TCP** introduces the term of **segments,** which are another type of
> containers as packets and frames are.

-   are encapsulated in packets

-   they do not have source and destination information because they the
    > IP packets for the transit

![](media/image144.jpeg){width="7.63125in"
height="0.8590277777777777in"}

it ensures that packets

> AWS Developer Page 88

![](media/image145.png){width="7.777083333333334in"
height="10.009722222222223in"}

> it ensures that packets
>
> are received in order
>
> indicates that the packet
>
> was received
>
> used to close the connection or synchronize The number of bites the
> receiver can receive
>
> error checking traffic control

![](media/image146.jpeg){width="7.616666666666666in"
height="3.457638888888889in"}

> AWS Developer Page 89

![](media/image147.png){width="7.7652777777777775in"
height="10.002083333333333in"}

**Stateless** firewall does not understand the state of a connection.

Rules

1.  Outbound: send -\> **OUT**

2.  Response: receive **-\> IN**

**Stateful** firewall understands the states of the TCP segments.

It sees the outbound and the response traffic as one, therefore once the
connection is established, it automatically allows the response.

![](media/image148.jpeg){width="4.634027777777778in"
height="0.5902777777777778in"}![](media/image149.jpeg){width="4.634027777777778in"
height="0.5902777777777778in"}

> AWS Developer Page 90

![](media/image150.png){width="4.779861111111111in"
height="10.002083333333333in"}

> AWS Developer Page 91

**Network Address Translation (NAT)**

+--------------------------------------------------+-------------------+
| Wednesday, June 9, 2021                          | > 3:51 PM         |
+==================================================+===================+
+--------------------------------------------------+-------------------+

AWS Developer Page 92

**Layer 5 - Session Layer**

+--------------------------------------------------+-------------------+
| Wednesday, June 9, 2021                          | > 1:40 PM         |
+==================================================+===================+
+--------------------------------------------------+-------------------+

AWS Developer Page 93

**Network Address Translation (NAT)**

+--------------------------------------------------+-------------------+
| Wednesday, June 9, 2021                          | > 4:14 PM         |
+==================================================+===================+
+--------------------------------------------------+-------------------+

> **NAT** is a process that is designed to address the growing shortage
> of IPv4 addresses.

![](media/image151.jpeg){width="5.8909722222222225in"
height="2.6708333333333334in"}

> **one to one**
>
> **one to many (from a pool)**

**many to one**

> **IPv6** does not need NAT, as there is **no** need for **private IP
> addressed**
>
> Static NAT
>
> Private IP addresses cannot communicate over the internet with the
> public IP addresses.

![](media/image152.jpeg){width="7.299305555555556in"
height="3.8291666666666666in"}

> **Is important to remember that in all the time, the two private
> devices, are never assigned any public IP address. The NAT device, is
> routing the packets to the private devices.**
>
> Dynamic NAT
>
> **Dynamic NAT is applied when there are not enough public IP addresses
> for all the private devices,**
>
> AWS Developer Page 94
>
> **therefore a pool of public IP address is temporary allocated and
> used as they are needed.**

![](media/image153.jpeg){width="7.389583333333333in"
height="3.9159722222222224in"}

> Port Address Translation (PAT)

![](media/image154.png){width="7.389583333333333in"
height="3.8958333333333335in"}

> AWS Developer Page 95

**IPv4 Addressing and Subnetting**

+--------------------------------------------------+-------------------+
| Wednesday, June 9, 2021                          | > 5:07 PM         |
+==================================================+===================+
+--------------------------------------------------+-------------------+

![](media/image155.jpeg){width="7.533333333333333in"
height="3.9590277777777776in"}

> **10.16.0.0 /16 (first 16 zeros in binary) - means that the last two
> octets are available for hosts or subnetting.**

1.  **starts are 10.16.0.0**

2.  **ends at 10.16.255.255**

![](media/image156.jpeg){width="6.639583333333333in"
height="3.2840277777777778in"}

+-----------------------------+----------------------------------------+
| > **/0**                    | > all internet                         |
+=============================+========================================+
|                             |                                        |
+-----------------------------+----------------------------------------+
| > **/8**                    | > class A                              |
+-----------------------------+----------------------------------------+
|                             |                                        |
+-----------------------------+----------------------------------------+
| > **/16**                   | > class B                              |
+-----------------------------+----------------------------------------+
|                             |                                        |
+-----------------------------+----------------------------------------+
| > **/24**                   | > class C                              |
+-----------------------------+----------------------------------------+
|                             |                                        |
+-----------------------------+----------------------------------------+
| > **/32**                   | > a single IP                          |
+-----------------------------+----------------------------------------+
|                             |                                        |
+-----------------------------+----------------------------------------+

<table style="width:100%;">
<colgroup>
<col style="width: 11%" />
<col style="width: 0%" />
<col style="width: 2%" />
<col style="width: 7%" />
<col style="width: 11%" />
<col style="width: 11%" />
<col style="width: 11%" />
<col style="width: 11%" />
<col style="width: 2%" />
<col style="width: 8%" />
<col style="width: 2%" />
<col style="width: 8%" />
<col style="width: 11%" />
</colgroup>
<thead>
<tr class="header">
<th colspan="2"><blockquote>
<p>10.16.0.0</p>
</blockquote></th>
<th></th>
<th
colspan="6"><strong>00001010.00010000</strong>.00000000.00000000/<strong>16</strong></th>
<th><blockquote>
<p>255</p>
</blockquote></th>
<th></th>
<th></th>
<th></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td></td>
<td
colspan="6"><strong>00001010.00010000.0</strong>0000000.00000000/17</td>
<td><blockquote>
<p>128</p>
</blockquote></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td></td>
<td
colspan="6"><strong>00001010.00010000.00</strong>000000.00000000/18</td>
<td><blockquote>
<p>64</p>
</blockquote></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td colspan="2"></td>
<td colspan="2"></td>
<td></td>
</tr>
<tr class="odd">
<td>1</td>
<td></td>
<td>2</td>
<td></td>
<td>4</td>
<td>8</td>
<td><blockquote>
<p>16</p>
</blockquote></td>
<td><blockquote>
<p>32</p>
</blockquote></td>
<td colspan="2"><blockquote>
<p>64</p>
</blockquote></td>
<td colspan="2"><blockquote>
<p>128</p>
</blockquote></td>
<td><blockquote>
<p>256</p>
</blockquote></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><blockquote>
<p>0</p>
</blockquote></td>
<td></td>
<td>1</td>
<td></td>
<td>0</td>
<td>1</td>
<td><blockquote>
<p>0</p>
</blockquote></td>
<td><blockquote>
<p>0</p>
</blockquote></td>
<td><blockquote>
<p>0</p>
</blockquote></td>
<td></td>
<td><blockquote>
<p>0</p>
</blockquote></td>
<td></td>
<td><blockquote>
<p>0</p>
</blockquote></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><blockquote>
<p>0</p>
</blockquote></td>
<td></td>
<td>0</td>
<td></td>
<td>0</td>
<td>0</td>
<td><blockquote>
<p>1</p>
</blockquote></td>
<td><blockquote>
<p>0</p>
</blockquote></td>
<td><blockquote>
<p>0</p>
</blockquote></td>
<td></td>
<td><blockquote>
<p>0</p>
</blockquote></td>
<td></td>
<td><blockquote>
<p>0</p>
</blockquote></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

> AWS Developer Page 96

**Distributed Denial of Service (DDos)**

+--------------------------------------------------+-------------------+
| Thursday, June 10, 2021                          | > 1:26 PM         |
+==================================================+===================+
+--------------------------------------------------+-------------------+

> DDoS are attacks designed to **overload** websites.

![](media/image157.jpeg){width="7.267361111111111in" height="3.4875in"}

> **Application Layer Attack**

![](media/image158.jpeg){width="7.250694444444444in"
height="3.807638888888889in"}

> **Protocol Attack - SYN Floods**

AWS Developer Page 97

![](media/image159.png){width="7.508333333333334in"
height="10.002083333333333in"}

> **Volume/Amplification Attack**

![](media/image160.jpeg){width="7.2756944444444445in"
height="3.8305555555555557in"}

> **The attacks cannot be avoided with normal network securities
> measures. Mitigating a DDoS attack, you need to be careful to not
> block real users!**

AWS Developer Page 98

**SSL and TLS**

+-------------------------------------------------+--------------------+
| Thursday, June 10, 2021                         | > 1:52 PM          |
+=================================================+====================+
+-------------------------------------------------+--------------------+

> **SSL -\>** Secure Sockets Layer
>
> **TLS -\>** Transport Layer Security
>
> They both focus on the **privacy** and **data integrity** between the
> **client** and the **server**.
>
> **Privacy - communication are encrypted (asymmetric)**
>
> **Identity verification - client/server verified**
>
> **Reliable connection - protection against alteration**

![](media/image161.jpeg){width="7.502777777777778in"
height="3.654166666666667in"}

> AWS Developer Page 99

**Virtual Private Clouds (VPC)**

+-------------------------------------------------+--------------------+
| Tuesday, June 15, 2021                          | > 3:56 PM          |
+=================================================+====================+
+-------------------------------------------------+--------------------+

> VPC is used to create private networks inside AWS, and is used to
> connect AWS private networks to the on premises networks when creating
> a hybrid environment.
>
> VPC is also the service that allows you to connect to other cloud
> platforms when creating a multi-cloud deployment.

![](media/image114.jpeg){width="0.14166666666666666in"
height="0.14166666666666666in"}

> **VPC** is a virtual network inside AWS.
>
> There are two types of VPC:

1.  Default VPC - **maximum** one per region and can be deleted, removed
    > or recreated

    a.  created by AWS

    b.  they come preconfigured in a very specific way

    c.  they are less flexible than custom VPCs

    d.  always have the CIDR: **172.31.0.0/16**

    e.  **everything placed in the VPC subjects is assigned a public
        > IPv4**

2.  Custom VPCs - as many as you want

    a.  they can be configured as they need to be

    b.  require the configuration, end to end in **detail**

    c.  they are **private** by default

![](media/image114.jpeg){width="0.14166666666666666in"
height="0.14166666666666666in"}

> VPCs **cannot communicate** in between them, even if they are in the
> same AWS account, unless is stated otherwise. Basically, VPCs are by
> default **entirely private.**
>
> Default VPC

![](media/image114.jpeg){width="0.14166666666666666in"
height="0.14166666666666666in"}

> Every VPC is allocated a range of IP addresses, called **VPC Cider**.
> Everything inside a VPC, uses the CIDER range of that VPC. Is anything
> needs to communicate with that VPC (if is allowed) it needs to
> communicate to that VPC CIDR.

![](media/image114.jpeg){width="0.14166666666666666in"
height="0.14166666666666666in"}

> The default VPC gets only one CIDR: **172.31.0.0/16**
>
> This is one of the strengths, is always configured by default in the
> same way:

-   has one subnet in every availability zone in its region

-   each subnet uses a part of the VPC\'s range of IP addresses

-   these cannot be the same or overlap as other subnets in the VPC

-   this makes the VPCs **resilient**

![](media/image162.jpeg){width="6.602777777777778in"
height="3.1708333333333334in"}

> Custom VPC
>
> Custom VPCs can have multiple CIDR ranges.
>
> AWS Developer Page 100

**Network IDs and Subject Masks**

+------------------------------------------------+---------------------+
| Tuesday, July 13, 2021                         | > 4:49 PM           |
+================================================+=====================+
+------------------------------------------------+---------------------+

> 192.168.1.0/24
>
> /24 is CIDR - tell you how many binary digits are turned on in a sub
> mask
>
> /**24** - \> **11111111.11111111.11111111**.00000000 - \>
> 255.255.255.0 **/16 - \> 11111111.11111111.**00000000.00000000 -\>
> 255.255.0.0
>
> **/32 - \> 11111111.11111111.11111111.11111111** -\> 255.255.255.255
>
> **Mask:** 255.255.248.0 -\> **11111111.11111111.11111000.00000000**
> -\> **/21**
>
> **192.168.40.55** - \> what is the network **ID**? can be used for the
> hosts
>
> Network ID: 192.168.40.0/21
>
> Sub mask: 255.255.248.0
>
> **Mask:** 255.255.255.192 - \> 11111111.11111111.11111111.11000000 -\>
> **/26**
>
> **192.128.45.55 -\> 11000000.10000000.00101101.00110111 Network ID:
> 192.128.45.0/26**

AWS Developer Page 101

**VPC Sizing and Structure**

+------------------------------------------------+---------------------+
| Tuesday, July 13, 2021                         | > 4:17 PM           |
+================================================+=====================+
+------------------------------------------------+---------------------+

> A **custom VPC** is a private network inside AWS.
>
> Creating a VPC

1.  decide the range the VPC will use - **VPC Cider**

    -   **more than one can be added -** [the IP range needs to be known
        > in **advance**]{.underline}

> Considerations

1.  What size the VPC should be?

    -   how many services can fit into that VPC

        -   each service has one or more IPs and those occupy space
            > inside the VPC

2.  Are there any other networks that we will **use** or **interact**
    > with

    -   overlapping or duplicate ranges will made the network
        > communication difficult

3.  What other **ranges** other a. VPCs use

    -   cloud environments

    -   premises networks

    -   partners or vendors

    -   **avoid ranges that are used by other party ranges use and that
        > you interact with**

4.  Try to predict the future

5.  Consider the structure of the VPC

    -   for a given IP range allocated to a VPC it will need to be
        > broken down further

    -   tiers: web tier, application tier, database tier - depend on the
        > VPC architecture

6.  Avoid common ranges

7.  **A good infrastructure is as much as good design as it is
    > technically implemented**

![](media/image38.jpeg){width="0.16666666666666666in"
height="0.16666666666666666in"}

> A **VPC** can be the **smallest /28** and the **maximum /16**
>
> Animals4Life example:

![](media/image163.jpeg){width="5.914583333333334in"
height="3.1305555555555555in"}

> When designing a VPC for the business, we cannot use any of this IP
> addresses spaces.

AWS Developer Page 102

> The Azure IP address is the same as the default VPC address

-   that means we cannot use the default VPC for anything in production

-   but that is okey, as when is possible we should avoid using the
    > default VPC

![](media/image38.jpeg){width="0.16666666666666666in"
height="0.16666666666666666in"}

> A **VPC** can be the **smallest /28** and the **maximum /16**
>
> **When creating a VPC:**

-   **CAUTION**

-   **use a 10. IP address**

    -   **10.0 NO - as is used by most used**

    -   **10.1 NO - as everyone uses this to avoid 10.0**

    -   **10.16 YES - would be a good start**

-   **when thinking about the number of networks a business will need**

    -   we will start at 10.16 and end at 10.128 because that is used by
        > Google

    -   the number of regions required can be determinates in how many
        > ranges a business requires

        -   in how many regions the business will ever operate in

        -   and then add a few as a buffer

    -   reserve 2+ networks per region being used per account

> VPC Sizing

![](media/image164.jpeg){width="6.347916666666666in" height="1.71875in"}

> Important questions
>
> *\"A subnet, or subnetwork, is a network inside a network. Subnets
> make networks more efficient. Through subnetting, network traffic can
> travel a shorter distance without passing through unnecessary routers
> to reach its destination.\"*

-   how many **subnets** will you need?

-   how many **IPs total**?

-   how many **per subnet**?

> Services run on subnets, not directly from VPC.

-   a subnet is allocated in one availability zone

    -   how many availability zone the VPC will use?

        -   this decision impacts availability an resiliency and it
            > depends somehow on the region the VPC is in

        -   is good to start with 3 availability zones

            -   is a good practice as it will work in almost any region

            -   is good to add a spare as things grow as time passes

            -   =\> **this means 4 availability zones**

        -   divide the VPC in 4 smaller networks: 4 subnets

            -   if we started at /16 we would have four /18 subnets

            -   each tier has its own subnet in its availability zone

> Remember:

![](media/image75.jpeg){width="0.16666666666666666in"
height="0.16666666666666666in"}

> Each time a prefix is increased, subnets are created

AWS Developer Page 103

-   from 16 to 17 it creates 2 networks

-   from 16 to 18 it creates 4 networks

-   from 16 to 19 it creates 8 networks

-   from 16 to 20 it creates 16 networks

![](media/image165.png){width="6.053472222222222in"
height="9.085416666666667in"}

AWS Developer Page 104

![](media/image166.png){width="5.524305555555555in"
height="10.011111111111111in"}

AWS Developer Page 105

![](media/image167.png){width="5.507638888888889in"
height="10.002083333333333in"}

AWS Developer Page 106

![](media/image168.png){width="5.5256944444444445in"
height="10.002083333333333in"}

AWS Developer Page 107

![](media/image169.png){width="5.527777777777778in"
height="10.002083333333333in"}

AWS Developer Page 108

![](media/image170.png){width="5.509027777777778in"
height="10.002083333333333in"}

AWS Developer Page 109

**Custom VPCs**

+--------------------------------------------------+-------------------+
| Wednesday, July 14, 2021                         | > 3:27 PM         |
+==================================================+===================+
+--------------------------------------------------+-------------------+

> One of the benefits of VPCs is that you can start up simple, and layer
> components piece by piece.

![](media/image171.jpeg){width="7.420833333333333in"
height="3.592361111111111in"}

> **VPC**s are regionally isolated and resilient service.
>
> ![](media/image172.jpeg){width="0.14027777777777778in"
> height="0.125in"}- is created in a region and it operates from all
> availability zones from that region
> ![](media/image173.jpeg){width="0.14027777777777778in"
> height="0.125in"}- it allows the creation of isolated networks in AWS

-   even in a single region within one account there can be multiple
    > isolated networks

> ![](media/image172.jpeg){width="0.14027777777777778in"
> height="0.125in"}- nothing is allowed **in** or **out** of a VPC
> without **explicit configuration**
>
> ![](media/image172.jpeg){width="0.14027777777777778in"
> height="0.125in"}- custom VPC has flexible configuration - simple and
> multi-tier

-   they also support hybrid networking - other cloud platforms and
    > on-premises networks

-   have default or dedicated tenancy - if resources inside a VPC are
    > having shared or dedicated hardware

> ![](media/image174.jpeg){width="0.14027777777777778in"
> height="0.14027777777777778in"}^▪^ **DEFAULT** - you can choose on a
> per resource basis later on when you provision resources as whether it
> goes on dedicated or shared hardware
>
> ![](media/image174.jpeg){width="0.14027777777777778in"
> height="0.14027777777777778in"}^▪^ **DEDICATED TENANCY** - it is
> locked in, any resources that are created inside the VPC
>
> have to be on dedicated hardware
>
> \- are using IPv4 private CIDR Blocks and public IPs

-   the private CIDR block is the main communication channel with the
    > VPC

    -   by default 1 primary private IPv4 CIDR block is allocated to a
        > VPC

```{=html}
<!-- -->
```
-   this has two restrictions:

> ![](media/image175.jpeg){width="0.14027777777777778in"
> height="0.125in"}1. at its smallest it can be /28 prefix (the entire
> VPC has 16 IP addresses)
>
> 2\. at its largest it can be /16 prefix (65,536 IP addresses)

-   other optional secondary IPv4 blocks can be added after creation

```{=html}
<!-- -->
```
-   public IPs are used when resources need to be made public

> \- it can be configured to use IPv6 by assigning /56 CIDR block to the
> VPC

![](media/image176.jpeg){width="0.14027777777777778in"
height="0.14027777777777778in"}

-   they do not have the concept of private or public - are all publicly
    > routable by default

    -   when used, explicit allow connectivity to and from the public
        > internet is required

```{=html}
<!-- -->
```
-   have fully featured DNS

    -   provided by Route53

    -   is available by the base IP address of the VPC + 2 (if the
        > address 10.0.0.0 the DNS will be 10.0.0.2)

    -   Two options for the DNS:

1.  **enableDnsHostNames** - this indicates weather instances with
    > public IP addresses in a VPC are given public DNS host names

    -   if is set to TREU, then instances do get a public DNS name

2.  **enableDnsSupport** - it indicates weather the DNS is enabled or
    > disabled in the VPC

> AWS Developer Page 110

-   if enabled then instances in the VPC can use the DNS IP address (VPC
    > +2 IP)

![](media/image177.jpeg){width="7.4840277777777775in"
height="4.020833333333333in"}

> AWS Developer Page 111

**VPC Subnets**

Thursday, July 15, 2021 11:23 AM

> **Subnets** are what services run from inside VPC [[Subnet Calculator
> \| IP Subnet Mask Calculator for IPv4 -
> Site24x7]{.underline}](https://www.site24x7.com/tools/ipv4-subnetcalculator.html)

-   how add structure, functionality and resilience to VPCs

![](media/image177.jpeg){width="7.440972222222222in"
height="3.997916666666667in"}

> This is the structure that was left off, since last lecture. (We only
> created a VPC). Today we will create an internet structure using
> subnets.
>
> By default subnets are **private** and they require some configuration
> to make it **public**.
>
> A **subnet** is a feature of VPC that is **AZ resilient** - a
> sub-network of the VPC.

-   **a is hosted in a AZ, if that AZ fails, that the subnet itself
    > fails**

-   to make a system highly-available, we put different components of
    > the system into different AZ , to make sure that if one AZ fails,
    > the whole system doesn't fail

    -   the way we do this, is to put different components in different
        > subnets, where each are located in a specific AZ

-   once a AZ has been chosen for a subnet

    -   it can never be changed

    -   and cannot spread over multiple AZs

> ![](media/image178.jpeg){width="0.14027777777777778in"
> height="0.11458333333333333in"}○ **one subnet is in one AZ**
>
> ![](media/image179.jpeg){width="0.13819444444444445in"
> height="0.125in"}- **an AZ can have zero to lots of subnets**

-   by default a subnet uses a IPv4 and is allocated an IP-version-four
    > CIDR

    -   the CIDR is a subset of the VPC CIDR block

    -   has to be in the range of IPs allocated to the VPC

> ![](media/image178.jpeg){width="0.14027777777777778in"
> height="0.11458333333333333in"}○ the CIDR used by a subnet cannot
> overlap other subnets

-   optionally IPv6 CIDR block can be allocated to a subnet

    -   as long as the VPC is also enabled for IPv6

    -   /64

-   subnets from a VPC can communicate with other subnets from the same
    > VPC

    -   the isolation happens at the permitter of the VPC, not inside it

    -   internally there is free communication between subnets by
        > default

-   some IP addresses inside subnets are reserved - hence they cannot be
    > used

+--------------+-------------------------------------------------------+
| > **there    | > example **10.16.16.0/20** (10.16.16.0 -\>           |
| > are 5 in   | > 10.16.31.255)                                       |
| > total**    |                                                       |
+==============+=======================================================+
| > **1. first | > **10.16.16.0** -\> represents the starting address  |
| > IP         | > of the network                                      |
| > address**  |                                                       |
+--------------+-------------------------------------------------------+
| > **2.       | > 1**0.16.16.1** -\> it is used by the VPC router     |
| > network +  |                                                       |
| > 1**        |                                                       |
+--------------+-------------------------------------------------------+

> AWS Developer Page 112
>
> ○

+--------------+-------------------------------------------------------+
|              | > • the logical network device which moves data       |
|              | > between subnets and **in** and                      |
+==============+=======================================================+
|              | > **out** of the VPC if is allowed                    |
+--------------+-------------------------------------------------------+
| > **3.       | > **10.16.16.2** -\> is used for DNS                  |
| > network +  |                                                       |
| > 2**        |                                                       |
+--------------+-------------------------------------------------------+
| > **4.       | > **10.16.16.3** -\> reserved for future requirements |
| > network +  |                                                       |
| > 3**        |                                                       |
+--------------+-------------------------------------------------------+
| > **5. last  | > **10.16.16.255** -\> used for broadcast             |
| > IP         |                                                       |
| > address**  |                                                       |
+--------------+-------------------------------------------------------+
|              | > • broadcast is not supported inside a VPC           |
+--------------+-------------------------------------------------------+
|              |                                                       |
+--------------+-------------------------------------------------------+

-   A VPC has a configuration object applied to it called a **DHCP
    > option set**

    -   stands for **Dynamic Host Configuration Protocol**

    -   is how computing devices receive IP address automatically

    -   controls the DNS servers, NTP servers, NET bile

    -   **you can create option sets, but you CANNOT edit them**

-   can be set two IP allocation options

1.  controls if resources are allocated a public IPv4 address in
    > addition to the private subnet

2.  controls if resources deployed into the subnet are also given a IPv6
    > address

> ○ both option are defined at a subnet level and flow on any resources
> inside that's subnet
>
> AWS Developer Page 113

**VPC Routing, Internet Gateway & Bastion Hosts**

+---------------------------------------------+------------------------+
| Friday, July 16, 2021                       | > 12:04 PM             |
+=============================================+========================+
+---------------------------------------------+------------------------+

> VPC Router
>
> A **VPC router** is a highly available device

-   is present in every VPC (default or custom)

-   moves traffic from point A to point B

-   it runs in all AZ that the VPC uses

-   has a network interface in every subnet in the VPC - **network + 1**

> ![](media/image39.jpeg){width="0.16666666666666666in"
> height="0.14583333333333334in"}- **without any configuration, the
> router simply routes traffic between subnets**

-   can create route tables which influence what to do with the traffic
    > when it leaves a subnet

    -   each subnet has it own route table

-   a VPC is created with a **main route table**

    -   when a route table is associated with a subnet, then the main
        > rout table is disassociated
        > ![](media/image180.jpeg){width="0.16527777777777777in"
        > height="0.13541666666666666in"}○ a subnet can **only have one
        > route table** associated with it!

> ![](media/image180.jpeg){width="0.16527777777777777in"
> height="0.13541666666666666in"}○ a route table can be associated with
> **many subnets**
>
> The process
>
> When traffic leaves the subnet that the route table is associated with

-   the VPC router reviews the IP packets

    -   packets they have a **source address** and a **destination
        > address** along with the data that is transmitted

-   the VPC router looks at the destination address of all packets
    > leaving the subnet

-   **checks the route table for a matching destination address**

    -   does this my checking the destination field of a route

        -   could match a specific IP

        -   could match a specific network

        -   could match a default route(0.0.0.0/0)

        -   if there are multiple matches, **then the prefix is used as
            > a priority**

            -   the higher the prefix value, the more specific the
                > routers and the higher priority that route has

    -   when a single route is selected, then the VPC router forwards
        > that traffic through its destination which is determined by
        > the **target** field on the route (local or AWS gateway)

        -   local - in the VPC it self

> ![](media/image181.jpeg){width="0.16527777777777777in"
> height="0.16666666666666666in"}^▪^ local routes always take priority
>
> Internet Gateway (IGW)
>
> **Internet Gateway** is one of the most important add-on features
> available within a VPC.
>
> \- it is a **region resilient** gateway that can be attached to a VPC

-   there is a one to one relationship between a VPC and gateways

    -   a VPC can have one internet gateway, or zero

    -   an internet gateway can have one VPC, or zero

-   it is at the boarder or the AWS Public Zone

-   allows traffic between the VPC and the Internet or the AWS public
    > zone

-   it is a manages service

-   AWS handles the performance

> The process

1.  we attach an internet gateway to a VPC

    -   it means that is available to be used for use inside the VPC

    -   we can use it as a target within the route tables

> AWS Developer Page 114

2.  we add the default route to the route\'s route table with its target
    > being the internet gateway

3.  we configure the subnets to allocate IPv4 and optionally IPv6

4.  the subnet is classified now as being a public subnet

    -   any services inside that subnet with public IP addresses can
        > communicate with the internet (and vice-versa)

    -   they also can communicate with the AWS public zone (as long as
        > there are no other security limitations)

![](media/image182.jpeg){width="7.177777777777778in"
height="2.5909722222222222in"}

> IPv4 addresses with Internet Gateway
>
> A public IPv4 (43.250.192.20 in our example) never touches the actual
> services inside a VPC.

-   a record of the address is created which the internet gateway
    > maintains ![](media/image180.jpeg){width="0.16527777777777777in"
    > height="0.13541666666666666in"}○ it links the private IP to its
    > allocated public IP

> ![](media/image94.jpeg){width="0.16527777777777777in"
> height="0.13541666666666666in"}○ the instance itself, is not allocated
> with the public IP - the gateway is

![](media/image183.jpeg){width="7.120833333333334in"
height="1.8833333333333333in"}

> The instance communicating with the Linux server:

![](media/image184.jpeg){width="7.084027777777778in"
height="1.2722222222222221in"}

> The Linux server communicates with the Instance:

![](media/image185.jpeg){width="7.194444444444445in"
height="0.6736111111111112in"}

> AWS Developer Page 115

![](media/image186.png){width="7.397222222222222in"
height="10.002083333333333in"}

> At any point, the OS on the EC2 instance is aware of the public IP
> address - the internet gateway is!

![](media/image187.jpeg){width="0.16666666666666666in"
height="0.16527777777777777in"}

> With IPv6 all IP address are natively publicly routable! - the OS does
> have the IPv6 address configure on it, and all the internet gateway
> does is to pass traffic from an instance to the internet server and
> back again
>
> Bastion Host / Jumpbox
>
> Bastion Host or Jumpbox is an instance in a public subnet

-   they are used to allow incoming management connection

-   when connected you can access internal-only VPC resources

-   are generally used as:

    -   management point

    -   entry point for private only VPC

![](media/image188.jpeg){width="7.2027777777777775in" height="3.8125in"}

AWS Developer Page 116

**Network Access Control Lists (NACLs)**

+-----------------------------------------------+----------------------+
| Saturday, July 17, 2021                       | > 11:47 AM           |
+===============================================+======================+
+-----------------------------------------------+----------------------+

> **Network Access Control Lists (NACLs)** are a security feature of AWS
> that is seen as a firewall which surrounds VPC subnets

-   all VPCs are created with a default network ACL associated with all
    > subnets in that VPC **by default**

-   NACLs are used when traffic enters or leaves a subnet

    -   because they are associated with subnets (and not services) they
        > are used when data crosses the subnet boundary

    -   are formed of two sets of rules

        -   **inbound**

        -   **outbound**

    -   **the rules are processed as:**

1.  in order - lowest rule first

2.  when a rule is matched an action is taken and the process has
    > stopped

    -   the rule can **allow** or **deny** the traffic to cross the
        > subnet permitter ^▪^ each rule has a number of fields:

    -   type, protocol, port range -\> are concerned with the type of
        > traffic going in or out (SSH, HTTP, HTTPS, and others)

    -   for inbound rules there is the source field - where the traffic
        > is coming from

    -   for outbound rules there is the destination field - where the
        > traffic is going to

> ![](media/image189.jpeg){width="0.15833333333333333in"
> height="0.1597222222222222in"} ^▪^ if all fields match, the first rule
> matched it determinates which action is taken: to allow or deny the
> traffic
>
> ![](media/image189.jpeg){width="0.15833333333333333in"
> height="0.1597222222222222in"} ^▪^ if no rule matches the traffic,
> then the traffic is denied
>
> ![](media/image190.jpeg){width="0.15833333333333333in"
> height="0.13541666666666666in"}□ **there is always an implicit deny**

-   the Asterix rule can never be removed, or edited
    > ![](media/image191.jpeg){width="0.15833333333333333in"
    > height="0.13541666666666666in"}□ processed if nothing else matches

```{=html}
<!-- -->
```
-   by default there is also a rule number 100 - that can be edited or
    > removed

    -   is an explicit catch-all allow - **never block any traffic**

![](media/image192.jpeg){width="7.167361111111111in"
height="3.463888888888889in"}

> These NACLs are the most difficult security feature inside a VPC
>
> ![](media/image193.jpeg){width="0.15833333333333333in"
> height="0.15833333333333333in"}- networks ACLs are stateless - they
> are unable to assess the state of communication between two entities
> on a network

-   initiation and response are seen intendent

> AWS Developer Page 117

-   they need two different rules: for the request and for the response
    > ![](media/image194.jpeg){width="0.15833333333333333in"
    > height="0.13541666666666666in"}- network ACLs only impact traffic
    > which **crosses a subnet border**

-   data that enters or leaves a subnet

> ![](media/image195.jpeg){width="0.15833333333333333in"
> height="0.13541666666666666in"}- can be used to explicitly allow and
> explicitly deny traffic
> ![](media/image195.jpeg){width="0.15833333333333333in"
> height="0.13541666666666666in"}- only support using IPs , networks,
> ports and protocols
>
> ![](media/image195.jpeg){width="0.15833333333333333in"
> height="0.13541666666666666in"}- they do not have any visibility of
> AWS logical resources
> ![](media/image195.jpeg){width="0.15833333333333333in"
> height="0.13541666666666666in"}- they can be used in conjunction with
> security groups
>
> ![](media/image195.jpeg){width="0.15833333333333333in"
> height="0.13541666666666666in"}- one subnet **is only associated with
> one** network ACL

-   if one subnet has not added a network ACL, they default to the
    > default network ACL of the

> VPC

-   it needs a network ACL at all times: the custom or the default one

> ![](media/image189.jpeg){width="0.15833333333333333in"
> height="0.1597222222222222in"}- rules are processed in order, and the
> Asterix (the explicit deny) is the last, and it applies if anything
> else does not match
>
> ![](media/image196.jpeg){width="0.1597222222222222in"
> height="0.14583333333333334in"}○ processing stops at the first
> matching rule
>
> AWS Developer Page 118

**Security Groups**

+-----------------------------------------------+----------------------+
| Saturday, July 17, 2021                       | > 12:21 PM           |
+===============================================+======================+
+-----------------------------------------------+----------------------+

> **Security groups** are somehow similar to NACLs, but hey operate at a
> higher level of the networking stack, and integrate with AWS product
> and services in a much closer way.

-   it is attached to a resource/service and not the subnet

-   they have two sets of rules

    1.  **inbound**

    2.  **outbound**

> ![](media/image39.jpeg){width="0.16666666666666666in"
> height="0.14583333333333334in"}- are stateful (opposite of stateless)

-   the request and the response are viewed as part of the same
    > communication

-   only one rule is required for an inbound communication - where the
    > return traffic is automatically included in this allow

```{=html}
<!-- -->
```
-   they match traffic almost the same as the ACL

    -   type of traffic, protocol, port range and source

> ![](media/image39.jpeg){width="0.16666666666666666in"
> height="0.14583333333333334in"}- they **understand logical resources**

-   they are not limited to IP and network

-   they can references services and resources

-   they can reference other security groups and even themselves

    -   having a rule for itself, it means that it matches anything
        > associated with itself

> ![](media/image104.jpeg){width="0.16666666666666666in"
> height="0.13541666666666666in"}- they have a **hidden implicit deny**

-   what is not stated as allowed is implicitly denied

-   they cannot explicitly deny - if is not allowed then is denied

```{=html}
<!-- -->
```
-   **NACLs** are usually used if products do not support security
    > groups (NAT gateways)

    -   are also used when you want to add **explicit denies**

    -   subnet protection

> ![](media/image78.jpeg){width="0.16666666666666666in"
> height="0.14583333333333334in"}- **security groups should be used for
> anything else**
>
> AWS Developer Page 119

**Network Address Translation (NAT) & NAT Gateway**

+-----------------------------------------------+-----------------------+
| Tuesday, July 20, 2021                        | > 10:55 AM            |
+===============================================+=======================+
+-----------------------------------------------+-----------------------+

> **Network Address Translation (NAT)**

-   is a set of different processes which can adjust IP packets by
    > changing their source or destination IP address

-   **IP masquerading** provides a whole private range of IP addresses
    > outgoing only access to the public internet and the public AWS
    > public zone **(incoming access does not work)**

> ![](media/image94.jpeg){width="0.16527777777777777in"
> height="0.13541666666666666in"}○ many **private IPv4** addresses to
> **one public IP address**

-   this is important, because IPv4 addresses do run out

> The internet gateway actually performs a type of NAT known as **static
> NAT**

-   how a resource is allocated with a public IPv4 address AWS has two
    > ways to implement NAT services:

> 1\. via EC2 instances - configured to provide the NAT gateway

-   the **NAT** gateway makes a record of the packet sent from an
    > instance

    -   destination, source address and other details which help the NAT
        > gateway identify the specific communication in the future -
        > **all this is recorded into a translation table**

    -   this is needed as multiple instances could be communicating at
        > once, and each instance would have multiple communication with
        > different public internet hosts

-   after the packet details had been stored in the translation table,
    > then the packet is adjusted by changing the source packet to match
    > the NAT Gateway IP address (with the public routable IP address)

-   the packet is now moved from the **NAT Gateway** to the **internet
    > gateway** by the VPC router

![](media/image92.jpeg){width="0.16527777777777777in"
height="0.16527777777777777in"}

> **If you need to give an instance its own public IPv4 address then the
> internet gateway is required If you want to give multiple private
> instances, outgoing access to the internet and the AWS public zone
> services, the both a NAT gateway and the internet gateway are
> needed.**

![](media/image92.jpeg){width="0.16527777777777777in"
height="0.16527777777777777in"}

-   the **NAT gateway** is needed to do the many to one translation

-   the **internet gateway** is needed to translate from the NAT gateway
    > IP address to a real public IPv4 address

> NAT Gateway Product

-   it needs to run from a public subnet as it needs to be assigned a
    > public IPv4 address

-   it uses a special type of IPv4 address called **Elastic IP - static
    > IPv4 Public**

    -   **IPs do not change**

    -   **they are allocated ina region and the be used for any
        > purpose**

> ![](media/image95.jpeg){width="0.16527777777777777in"
> height="0.14583333333333334in"}- **are AZ resilient service**
>
> ![](media/image197.jpeg){width="0.16527777777777777in"
> height="0.16319444444444445in"}○ to make it mirror the internet
> gateway, then a NAT gateway is needed in each AZ that is used by a VPC
> and then have a route table for the private subnets in that AZ
> pointing at the NAT gateway in the AZ
>
> ![](media/image198.jpeg){width="0.16527777777777777in"
> height="0.16527777777777777in"}○ so for every AZ used, a NAT gateway
> is needed and one route table pointing at that NAT gateway
>
> ![](media/image199.jpeg){width="0.16527777777777777in"
> height="0.13541666666666666in"}○ **for maximum availability a NAT
> gateway needs is needed in every AZ**
> ![](media/image94.jpeg){width="0.16527777777777777in"
> height="0.13541666666666666in"}- **they are a managed service**

-   after they are deployed AWS handles everything else

-   they scale up to 45 GB/second in bandwidth

-   more gateways can be created

-   you cannot connect to its OS

```{=html}
<!-- -->
```
-   they are billed by the number that you have

    -   there is an hourly charge for running a NAT gateway

    -   partial hours are billed as full hours

    -   is billed also per gigabyte of processed data with the same
        > charge (as per hour)

> NAT Instance vs. NAT Gateway
>
> AWS Developer Page 120
>
> NAT Instance vs. NAT Gateway

![](media/image200.png){width="7.052777777777778in" height="3.59375in"}

> NAT instance, has a feature called **source and destination checks**,
> which drops any traffic that does not match the source or the
> destination network card of that
>
> NAT instances and gateways are similar as:

-   they both need a public IP address

-   they both need to run a public subnet

-   they both need a functional internet gateway

![](media/image201.jpeg){width="0.16527777777777777in"
height="0.16319444444444445in"}

> in most situations, a **NAT gateway** is the bets choice when a NAT is
> needed. However, there are a few configurations where using an **EC2
> based NAT instance** should be considered :

1.  if availability, bandwidth, low level of maintenance and high
    > performance are valued then **NAT gateway** should be used

> ![](media/image198.jpeg){width="0.16527777777777777in"
> height="0.16527777777777777in"}^▪^ A NAT gateway offers high end
> performance, it scales and its custom designed to
>
> perform network address translation
>
> ![](media/image198.jpeg){width="0.16527777777777777in"
> height="0.16527777777777777in"}^▪^ A NAT instance is limited by the
> capabilities of the instance it is running on.
>
> ![](media/image202.jpeg){width="0.16527777777777777in"
> height="0.16527777777777777in"}^▪^ A NAT instance is general purpose,
> so it won\'t offer the same level of custom design performance
>
> ![](media/image198.jpeg){width="0.16527777777777777in"
> height="0.16527777777777777in"}^▪^ A NAT instance is a single EC2
> instance running inside a AZ, so if the EC2 hardware or its AZ fails,
> the NAT instance will fail

-   **Benefits** if NAT instances:

    -   inside an AZ is highly available

    -   it will automatically recover

    -   it will automatically scale

    -   you can connect to them like to any other EC2 instance

> ![](media/image203.jpeg){width="0.16527777777777777in"
> height="0.14583333333333334in"}□ **NAT instances are only EC2
> instances, therefore you can filter the traffic using**
>
> **ACLs on the subnet the instance is in or security groups directly
> associated with that instance**

![](media/image94.jpeg){width="0.16527777777777777in"
height="0.13541666666666666in"}□ **NAT gateways do not support security
groups - you can only use NACLs with it**

-   NAT instance is cheaper especially with high volumes of data

> IP version 6

![](media/image204.jpeg){width="0.16527777777777777in"
height="0.1638888888888889in"}

> **NAT gateway** is not required and they do not function with IPv6
> because inside AWS all IPv6

AWS Developer Page 121

> addresses are publicly routable

![](media/image205.jpeg){width="0.16527777777777777in"
height="0.16527777777777777in"}

> ::/0 in the internet gateway will allow bidirectional network access
> to that instance
>
> SSH Forwarding

1.  We have the private client on the public internet, the bastion in
    > the middle and the private subnet on the right

2.  a client private key is stored on the laptop which is used to
    > connect to the bastion

3.  a public key is stored on the bastion and the private server

4.  on the client we have the SSH agent (which usually is present by
    > default)

    -   the command **ssh-add** and this adds our private key into the
        > agent

    -   it is stores securely and guarded carefully - but is still a
        > copy of the key inside the ssh agent

5.  when connecting to the bastion, using the special command ssh -A

    -   this creates a separate channel of communication between the
        > client and the bastion and allows the bastion to connect to
        > the SSH agent running on the client laptop for authentication

6.  then when we create an interaction between the bastion and the
    > private server

7.  the private server asks the bastion to prove the identity of the
    > user connecting (which normally will need a copy of the private
    > key from the bastion)

8.  the bastion forwards the request to the ssh agent, as it can prove
    > the identity as it has a copy of the private key

    -   the private key never leaves the client machine

![](media/image206.jpeg){width="6.4375in" height="3.4625in"}

> AWS Developer Page 122

**Elastic Compute Cloud - EC2**

+-------------------------------------------------+--------------------+
| Tuesday, June 15, 2021                          | > 6:02 PM          |
+=================================================+====================+
+-------------------------------------------------+--------------------+

> EC2 provides access to virtual machines known as instances.
>
> **EC2** is **IAAS** (infrastructure as a service)

-   provides access to virtual machines (EC2 instances)

-   an instance is an OS configured in a certain way with a certain set
    > of allocated resources

-   is a private AWS service by default

-   for public access to an EC2 instance than the VPC running needs to
    > support that public access

-   is AZ resilient

-   the developer managers the OS and everything up from the
    > infrastructure stack

-   is an on-demand billing by second or hour

-   instance charge are present such as:

    -   running the instance

    -   storage

    -   commercial software

-   storage is of 2 types

    -   on host storage - where the instance runs

    -   EBS Elastic Block Store - network storage made available for the
        > instance

> ECS has **few** states

-   **running**

-   **stopped**

-   **terminated** - one time action, that deletes the allocated storage

![](media/image207.jpeg){width="4.470833333333333in"
height="1.9986111111111111in"}

> **AMAZON MACHINE IMAGE (AMI)**

-   **is an image of an EC2 instance**

-   is used to create an EC2 instance

-   can be created from an EC2 instance

-   contains attached permissions that control which accounts can or
    > can\'t use the AMI

-   can be public

-   can be private (owner)

    -   explicit permissions can be granted from the owner to other
        > users

-   contains the root volume (partition) - the driver that boots the OS

-   can contains other volumes (other drivers)

-   contains block device mapping

    -   a configuration which link the volumes that the AMI has, and how
        > they are linked withing

> the OS
>
> **Windows** **Linux**

AWS Developer Page 123

-   a configuration which link the volumes that the AMI has, and how
    > they are linked withing

> the OS
>
> **Windows** **Linux**
>
> \- **remote desktop control port 3389** - **SHH protocol port 22**
>
> **What Permissions options does an AMI have?**
>
> **Public access, Owner Only, Specific AWS accounts**

AWS Developer Page 124

**Virtualization 101**

+-------------------------------------------------+--------------------+
| Wednesday, July 21, 2021                        | > 12:00 PM         |
+=================================================+====================+
+-------------------------------------------------+--------------------+

> **EC2** provides virtualization as a service - IAAS
>
> **Virtualization** is the process of running more than one Operating
> System on a piece of physical hardware
>
> In traditional OS:

-   the **kernel** from the OS is the only peace of software that is
    > able to interact with the hardware

    -   also, it runs in **privileged mode**

-   on top of the OS are **application** which are running in **user
    > mode**

    -   they cannot interact with the hardware, they need to go through
        > the OS

![](media/image208.jpeg){width="6.674305555555556in"
height="2.1305555555555555in"}

> With **virtualization:**

-   a single piece of hardware running multiple Operating Systems

    -   each OS is separate

    -   each OS runs its own applications

> Virtual Machines

![](media/image209.jpeg){width="6.674305555555556in"
height="2.5972222222222223in"}

> Para-Virtualization

![](media/image210.jpeg){width="6.645833333333333in"
height="1.2368055555555555in"}

AWS Developer Page 125

![](media/image211.png){width="6.848611111111111in"
height="10.002083333333333in"}

> The guest OS makes calls to the hypervisor, not to the hardware
>
> Hardware Assisted Virtualization

-   the hardware became virtualization aware

    -   the CPU is aware that it\'s performing virtualization

    -   when guest OS attempt to run any privileged instructions
        > they\'re trapped by the CPU which knows to expect them from
        > the guest OS

    -   the guest OS still believe they are running directly on the
        > hardware

![](media/image212.jpeg){width="6.747916666666667in"
height="4.159027777777778in"}

> Even this was a big improvement, for IO tasks, there are still
> obstacles to run smoothly as there is always software getting in the
> way of the guest OS, which impacts performance and consumes a lot of
> CPU cycles on the host OS.
>
> Single Route IO Virtualization (SR-IOV)
>
> SR-IOV allows any add on card (like networking card) to present it
> self as several mini cards. Because of this, there is no translation
> required by the hypervisor. The guest OS can directly use the its card
> whenever it wants.
>
> The physical card that supports this feature, handles the process end
> to end, making sure that when the guest OS use their logical mini
> network cards that they have physical access to the physical network
> connection when required.

AWS Developer Page 126

![](media/image213.png){width="6.991666666666666in"
height="10.002083333333333in"}

> In EC2 this feature is called **Enhanced Networking**, offering

-   faster speed

-   lower latency

-   lower latency at high loads

AWS Developer Page 127

**EC2 Architecture and Resilience**

+-------------------------------------------------+--------------------+
| Wednesday, July 21, 2021                        | > 12:47 PM         |
+=================================================+====================+
+-------------------------------------------------+--------------------+

> **EC2** instances are **virtual machines** (OS + Resources). It is the
> default compute service in AWS

![](media/image38.jpeg){width="0.16666666666666666in"
height="0.16666666666666666in"}

> **EC2** is great when you have a traditional OS and Application
> Compute need. SO if you have an application that requires to run on a
> certain OS with a certain runtime and configuration. It is also great
> for long running compute needs - **to run 24/7, 365**

![](media/image214.png){width="0.16666666666666666in"
height="0.35347222222222224in"}

> They are also perfect for applications or services that need burst
> requirements or steady-state requirements

![](media/image38.jpeg){width="0.16666666666666666in"
height="0.16666666666666666in"}

> Is great to use EC2 if you have a monolithic application - that uses a
> stack, database, middleware or other run-time based components, and is
> needs a Traditional OS EC2 is very useful for application workloads or
> disaster recovery

![](media/image38.jpeg){width="0.16666666666666666in"
height="0.16666666666666666in"}

-   they run on **EC2 hosts**

    -   are physical hardware that are managed by AWS

    -   these hosts can be

        1.  **Shared Hosts**

            -   these are shared between different AWS customers

            -   even resources are shared, each customer is isolated
                > from other customers

                -   there is no visibility, interaction between
                    > customers

            -   you do not get ownership of the hardware

            -   you pay for the individual instances based on how long
                > you run them for and what resources they have
                > allocated

            -   are the default option

        2.  **Dedicated Hosts**

            -   you are paying for the entire host not for the instances
                > that run on it

            -   you do no share it with other customers

> ![](media/image39.jpeg){width="0.16666666666666666in"
> height="0.14583333333333334in"}- is an **Availability Zone resilient
> service**
>
> ![](media/image78.jpeg){width="0.16666666666666666in"
> height="0.14583333333333334in"}○ if the AZ fails, the instance fails
>
> ![](media/image38.jpeg){width="0.16666666666666666in"
> height="0.16666666666666666in"}○ the service is very reliant on AZ, as
> the host and most of its dependencies need to be in the same AZ

-   have some local hardware:

    -   CPU

    -   memory

    -   local storage - instance store - is temporary

        -   is not portable

    -   storage networking

        -   can make use of remote storage

        -   can connect to the Elastic Block Store, which is known as
            > EBS

            -   EBS also runs inside a AZ

            -   they cannot be accessed crossed zone

            -   allows the creation and allocation of volumes -
                > persistent storage

    -   data networking

> ![](media/image38.jpeg){width="0.16666666666666666in"
> height="0.16666666666666666in"}^▪^ when instances are provisioned into
> a specific subnet, within a VPC, a Primary Elastic Network Interface
> is provisioned in a subnet (which are also AZ resilient) which maps to
> the physical hardware on the EC2 host
>
> ![](media/image38.jpeg){width="0.16666666666666666in"
> height="0.16666666666666666in"}^▪^ instances can have multiple network
> interfaces even in different subnets as long as **they are in the same
> AZ**

-   **instances** run on a specific host, and if they are restarted they
    > will stay on the same host

    -   they stay on a host until two things happened:

        1.  the host fails or is taken down for maintenance by AWS

        2.  if an instance is **stopped** and the **started**

![](media/image215.jpeg){width="0.16666666666666666in"
height="5.208880139982502e-3in"}

AWS Developer Page 128

> ![](media/image38.jpeg){width="0.16666666666666666in"
> height="0.16666666666666666in"} ^▪^ **if any of this two conditions
> happens, then the instance will be moved to another host, but on the
> same Availability Zone**

-   instances cannot natively move between AZ

    -   there are ways to do a migration but on the basics, it means
        > that a copy of the instance is

> moved to another AZ
>
> ![](media/image38.jpeg){width="0.16666666666666666in"
> height="0.16666666666666666in"}- **you can never** connect an instance
> to EBS or network interfaces in **another AZ**
> ![](media/image216.jpeg){width="0.16666666666666666in"
> height="0.13541666666666666in"}○ you cannot cross AZ with EBS or EBS
> volumes

-   instances running on a host, share the resources of that host

    -   instances of different sizes can share a host but generally
        > instances of the same type and generation will occupy the same
        > host

AWS Developer Page 129

**Instance Types**

+--------------------------------------------------+-------------------+
| Wednesday, July 21, 2021                         | > 1:56 PM         |
+==================================================+===================+
+--------------------------------------------------+-------------------+

> Instance types will influence different things:

-   the raw amount of resource that you get for that instance: virtual
    > CPU, memory, local storage capacity, and the type of the storage

    -   resource ratios

    -   the pay/minute in influenced by the raw amount of resources

-   influences the amount of network bandwidth for storage and data
    > networking capability you get

-   influences the architecture of the hardware that instances run on
    > and the vendor (ARM, x86)

-   influences any additional features and capabilities

> EC2 are grouped in 5 big categories:

1.  **General Purpose** - should always be the starting point

    -   designed for steady work loads

    -   have even ratios for resources

    -   should be the first choice, and you should move away from that
        > if there is a specific workload requirement

2.  **Compute Optimized** - designed for media processing, high
    > performance computing, scientific modeling, gaming and machine
    > learning

    -   they provide access to the latest high performance CPU

    -   offer a ratio where more CPU is offered for the memory

3.  **Memory Optimized -** is the inverse of the **compute optimized**

    -   offers large memory allocations for a given CPU amount

    -   it is ideal for application which need to work with large in
        > memory data sets, memory cashing, etc

4.  **Accelerated Computing** - additional capabilities come into play

    -   dedicated CPUS for high scale parallel processing

    -   custom programmable hardware such as FPGAs

5.  **Storage Optimized** - they provide large amounts of super-fast
    > local storage

    -   designed for high sequential transfer rates

    -   designed to provide massive amounts of IO operation per second

    -   is great for application with serios demands on sequential and
        > IO: databases, warehousing, elastic search, analytics
        > workloads

![](media/image217.jpeg){width="1.8819444444444444in"
height="0.9388888888888889in"}

> **R5dn.8xlarge** - is a name of a type of instance

-   **R** - is the instance family

-   **5** - is the generation (always use the last generation)

-   **8xlarge** - the instance size

-   **dn** - additional capabilities (might exist in the name or not)

> AWS Developer Page 130

![](media/image218.png){width="7.602083333333334in"
height="10.002083333333333in"}

> AWS Developer Page 131

**Storage Refresher**

+--------------------------------------------------+-------------------+
| Wednesday, July 21, 2021                         | > 4:15 PM         |
+==================================================+===================+
+--------------------------------------------------+-------------------+

> Key Storage Terms

-   **Direct** (local) attached Storage

    -   which are physical disks connected directly to a device

    -   for EC2 they are directly connected to the EC2 host and is
        > called **Instance Store**

    -   it is super-fast as it is attached directly to the hardware

    -   if the disk fails the storage can be lost

    -   if the hardware fails the storage can be lost

    -   if the instance moves between hosts the storage can be lost

-   **Network** attached Storage

    -   here is where volumes are created and attached to a device over
        > the network

    -   in AWS it uses a product called Elastic Block Store (EBS)

    -   it is highly resilient

    -   it is separate from the instance hardware

        -   can survive issues which impact the EC2 host

-   **Ephemeral** Storage

    -   temporary storage - storage that does not exist long term

    -   cannot rely on to be persistent

    -   an example is: instance storage

-   **Persistent** Storage

    -   storage which exists as its own thing

    -   it lives longer than the device that is attached to

    -   an example is: network attached storage delivered by EBS

> 3 Main Categories of Storage Available
>
> Describe how the storage is presented - to you or to a server - and
> what it can be used for

1.  **Block Storage**

    -   you can create a volume (eg. inside EBS)

    -   a block storage has a number of addressable blocks

    -   the block can have a huge or small number of blocks depending on
        > the size of the volume

    -   **the blocks are presented logically as a volume, or a hard
        > drive**

    -   they come in the form of **spinning hard disks or SSD** -
        > physical media or delivered as a **logical volume** which is
        > itself backed by different types of physical storage

        -   network attached storage systems provide block storage

    -   has no inbuild structure - it is a collection of uniquely
        > addressable blocks

        -   is up to the OS to create the file system and to mount that
            > file system

    -   you **can boot** from a block storage, and can save files to it

2.  **File Storage**

    -   it is provided by a file server

    -   you can access, request, traverse, search a file storage

    -   you cannot boot from a file storage

    -   can be mounted

3.  **Object Storage**

    -   used to store objects

    -   there is no structure is a flat collections of objects

    -   an object can be anything (key:value pair)

    -   not bootable

    -   not mountable

    -   it is scalable - can be accessed by millions of people
        > simultaneously

> AWS Developer Page 132
>
> Storage Performance

![](media/image219.jpeg){width="7.194444444444445in"
height="0.7416666666666667in"}

+--------------------+-------------------------+----------------------+
| > **IO (Block)     | > **Input-Output        | **Throughput**       |
| > Size**           | > operations per second |                      |
|                    | > -**                   |                      |
+====================+=========================+======================+
|                    | > **IOPS**              | (amount of data      |
|                    |                         | transferred at a     |
+--------------------+-------------------------+----------------------+
|                    |                         | given second -       |
|                    |                         | MB/second)           |
+--------------------+-------------------------+----------------------+
| > the size of the  | > measures the IO       | > is the rate of     |
| > blocks of data   | > operations the        | > data a storage     |
| > that             | > storage               | > system             |
+--------------------+-------------------------+----------------------+
| > can be written   | > system can support in | > can store on a     |
| > on the disk      | > a second. How         | > particular piece   |
|                    |                         | > of                 |
+--------------------+-------------------------+----------------------+
| > \- it can range  | > many reads/writes the | > storage            |
| > from pretty      | > storage system can    |                      |
+--------------------+-------------------------+----------------------+
| > small sizes (KB) | > accommodate in a      |                      |
| > to large         | > second                |                      |
+--------------------+-------------------------+----------------------+
| > ones (MB)        |                         | > generally          |
|                    |                         | > expressed in       |
|                    |                         | > MB/second          |
+--------------------+-------------------------+----------------------+
|                    |                         |                      |
+--------------------+-------------------------+----------------------+

> AWS Developer Page 133

**Elastic Block Store (EBS) Service Architecture**

+----------------------------------------------+-----------------------+
| Sunday, July 25, 2021                        | > 12:26 PM            |
+==============================================+=======================+
+----------------------------------------------+-----------------------+

> **EBS** is a service that provides block storage (storage that can be
> addressed using block IDs).

-   raw disk allocations - volume which can be encrypted using KMS

-   volumes when attached to EC2 instances they are seen as raw storage
    > and can be used to create a file system in top of it (ext3, ext3,
    > XFS and more)

-   they appear as any other storage device to an EC2 storage

> ![](media/image39.jpeg){width="0.16666666666666666in"
> height="0.14583333333333334in"}- storage **is provisioned in one AZ**
> (is separate and isolated in one AZ)
>
> ![](media/image39.jpeg){width="0.16666666666666666in"
> height="0.14583333333333334in"}○ they can be backed up to an S3 bucket
> in a form of a snapshot **which are regional**
>
> **resilient**
>
> ![](media/image75.jpeg){width="0.16666666666666666in"
> height="0.16666666666666666in"}^▪^ very useful to migrate data between
> availability zones

-   can be **replicated to other regions**

```{=html}
<!-- -->
```
-   they are created and attached to an EC2 instance **over a storage
    > network**

    -   it can be attached to multiple EC2 instances at the same time,
        > using a featured **called multi attached**

    -   needs to be managed to prevent over-writing at the same time
        > from different instances

-   they can be de-attached from one instance, and the re-attached to
    > another

    -   are not linked to the EC2 instance life cycle of one instance

-   it is persistent until **the volume is deleted**

-   **can provision data based on different physical storage types**
    > (SSD based, high performance SSD and volumes based on HDD)

    -   can also provision different sizes of volumes, different
        > performance

-   they are billed on GB/month metric, and in some cases on performance
    > characteristics

> ![](media/image78.jpeg){width="0.16666666666666666in"
> height="0.14583333333333334in"}- **volumes cannot be attached to
> instances from other AZ!**

AWS Developer Page 134

**EBS Volume Types - General Purpose**

+----------------------------------------------+-----------------------+
| Sunday, July 25, 2021                        | > 12:47 PM            |
+==============================================+=======================+
+----------------------------------------------+-----------------------+

> **EBS Volume Types**
>
> General Purpose SSD - GP2

-   is the default general purpose SSD based storage

-   is a high performance storage for a low price

-   has a throughput of 250 MB/second When is created:

    -   minimum storage is **1GB** and the maximum storage is **16 GB**

    -   created with an IO credit allocation (16 KB data)

        -   has a capacity of 5.4 million IO credits and it fills at the
            > baseline performance rate of the volume

        -   if you consume more IO credits than the rate at which the
            > bucket is filling, then you are using up the resources of
            > the bucket

        -   the maximum IO/second is 16,000

![](media/image220.jpeg){width="6.7027777777777775in"
height="3.5493055555555557in"}

-   is **great for boot volumes, low latency interactive apps** and for
    > **dev and test environments**

    -   it is currently the default

> General Purpose SSD - GP3

-   is also SSD based but it **removes the credit bucket architecture of
    > GPS2**

-   starts with a standard of 3000 IOPS (3,016 KB operation/second)

    -   can transfer 125 MB/second

    -   is standard regardless of the volume size - 1200MB/second

-   can safely swap between GP2 to GP3 at any point

> ![](media/image104.jpeg){width="0.16666666666666666in"
> height="0.13541666666666666in"}○ just remember that over 3000/IOPS the
> performance does not get added automatically

![](media/image39.jpeg){width="0.16666666666666666in"
height="0.14583333333333334in"}○ with GP3 the extra IOPS need to be
added manually which come at an extra cost

AWS Developer Page 135

**EBS Volume Types - Provisioned IOPS**

+------------------------------------------------+---------------------+
| Sunday, July 25, 2021                          | > 1:15 PM           |
+================================================+=====================+
+------------------------------------------------+---------------------+

> There are **3 types of provisioned IOPS SSD:**

-   what they have in common is that they can be configured
    > independently of the size of the volume

-   they are designed for super high performance situations

    -   consistent low latency and jitter

> ![](media/image39.jpeg){width="0.16666666666666666in"
> height="0.14583333333333334in"}○ IO1 and IO2:

-   64,000 IOPS/volume

-   1000 MB/s throughput

-   volume size range from 4GB to 16TB
    > ![](media/image38.jpeg){width="0.16666666666666666in"
    > height="0.16666666666666666in"}○ IO2 block express

-   256,000 IOPs/volume

-   4,000 MB/s throughput

-   volume size range from 4GB to 64TB

```{=html}
<!-- -->
```
-   there is a maximum performance which can be achieved between the EBS
    > service and a single EC2 instance

    -   this can be influenced by:

        -   the type of volume

        -   the type of the instance

        -   the size of the instance

-   **should be used for anything that needs really low latency, or sub
    > millisecond latency, consistent latency and high levels of
    > performance**

    -   **when you need smaller volumes but super high performance**

    -   **when maximum consistent IOPS is a priority**

    -   **when data is importanr**

> IO1

-   **50 IOPS/GB** of volume size

-   per instance performance 260,000 IOPS/instance and a throughput
    > 7,500 MB/s ![](media/image104.jpeg){width="0.16666666666666666in"
    > height="0.13541666666666666in"}○ you need 4 volumes to achieve
    > this per instance limit

> IO2

-   **500 IOPS/GB** of volume size

-   per instance performance 160,000 IOPS/instance and throughput of
    > 4,750MB/s

> IO2 - Block Express

-   **1000 IOPS/GB** of volume size

-   per instance performance 260,000 IOPs/instance and throughput 7,500
    > MB/s

AWS Developer Page 136

**EBS Volume Types - HDD-Based**

+------------------------------------------------+---------------------+
| Sunday, July 25, 2021                          | > 1:31 PM           |
+================================================+=====================+
+------------------------------------------------+---------------------+

> HDD based means that the storage has moving parts such a spinning
> platers (disks)

-   therefore they are slower

> There are two types of HDD storage within EBS

+----------------------------------------+-----------------------------+
| > Throughput Optimized - ST1           | > Cold HDD - SC1            |
+========================================+=============================+
| > fast but not agile                   | > is cold                   |
+----------------------------------------+-----------------------------+
| > is cheaper than SDD volumes which    | > is even cheaper but comes |
| > makes it ideal for                   | > with                      |
+----------------------------------------+-----------------------------+
| > any larger volumes of data           | > significant trade-offs    |
+----------------------------------------+-----------------------------+
|                                        | > \- is the lowest cost EBS |
|                                        | > storage                   |
+----------------------------------------+-----------------------------+
|                                        | > available                 |
+----------------------------------------+-----------------------------+
| > is designed for data which is        |                             |
| > sequentially accessed                |                             |
+----------------------------------------+-----------------------------+
| > \- is not great at random access     |                             |
+----------------------------------------+-----------------------------+
| > \- designed for data that needs to   |                             |
| > be written or read                   |                             |
+----------------------------------------+-----------------------------+
| > in a sequential way                  |                             |
+----------------------------------------+-----------------------------+
| > \- where economy is more important   |                             |
| > that IOPS and                        |                             |
+----------------------------------------+-----------------------------+
| > extreme performance                  |                             |
+----------------------------------------+-----------------------------+
| > volumes ca be from 125GB to 16TB in  | > volumes ca be from 125GB  |
| > size                                 | > to 16TB in size           |
+----------------------------------------+-----------------------------+
| > maximum of 500 IOPS (on 1MB block) - | > maximum of 250 IOPS (on   |
| > maximum                              | > 1MB block) -              |
+----------------------------------------+-----------------------------+
| > 500MB/s throughput                   | > maximum 250MB/s           |
|                                        | > throughput                |
+----------------------------------------+-----------------------------+
| > they work with a credit bucket with  | > they work with a credit   |
| > MB/S                                 | > bucket with MB/S          |
+----------------------------------------+-----------------------------+
| > \- base line performance 40MB/S for  | > \- baseline performance   |
| > every 1TB of                         | > 12MB/S for                |
+----------------------------------------+-----------------------------+
| > volume size                          | > every 1 TB of volume size |
+----------------------------------------+-----------------------------+
| > \- burst maximum of 250 MB/S for     | > \- burst maximum of       |
| > every 1TB volume                     | > 80MB/S for                |
+----------------------------------------+-----------------------------+
| > size                                 | > every 1TB volume size     |
+----------------------------------------+-----------------------------+
| > is designed:                         | > is designed:              |
+----------------------------------------+-----------------------------+
| > \- for when cost is a concern but    | > \- for infrequent         |
| > you need frequent                    | > workloads                 |
+----------------------------------------+-----------------------------+
| > access storage for throughput        | > \- if it geared for       |
| > intensive sequential                 | > maximum economy           |
+----------------------------------------+-----------------------------+
| > workloads                            | > when you just want to     |
|                                        | > store lots of             |
+----------------------------------------+-----------------------------+
| > \- big data, data warehouses and log | > data and do not care      |
| > processing                           | > about                     |
+----------------------------------------+-----------------------------+
|                                        | > performance               |
+----------------------------------------+-----------------------------+
|                                        | > \- archives, colder data, |
|                                        | > anything that             |
+----------------------------------------+-----------------------------+
|                                        | > requires less than a few  |
|                                        | > loads or                  |
+----------------------------------------+-----------------------------+
|                                        | > scan/day                  |
+----------------------------------------+-----------------------------+
|                                        |                             |
+----------------------------------------+-----------------------------+

AWS Developer Page 137

**Instance Store Volumes - Architecture**

+------------------------------------------------+---------------------+
| Sunday, July 25, 2021                          | > 1:58 PM           |
+================================================+=====================+
+------------------------------------------------+---------------------+

> **Instance Store Volumes** provide block storage devices.

-   raw volumes which can be attached to an instance presented to the OS
    > on that instance and

> used as the basis for a file system which can then in turn be used by
> application ![](media/image104.jpeg){width="0.16666666666666666in"
> height="0.13541666666666666in"}- they are local, **not over the
> network**

-   they are physically connected to the EC2 host

-   they are isolated to that one particular host

```{=html}
<!-- -->
```
-   they offer the highest storage performance available on AWS

    -   more than IBS can provide

> ![](media/image39.jpeg){width="0.16666666666666666in"
> height="0.14583333333333334in"}- included in the price of any instance

-   difference instance types come with different selections of instance
    > store volumes
    > ![](media/image104.jpeg){width="0.16666666666666666in"
    > height="0.13541666666666666in"}- they need to be attached at
    > launch time

-   they cannot be attached afterwards

```{=html}
<!-- -->
```
-   each instance can have a collection of volumes which are backed by
    > physical devices on the EC2 host

-   if an instance moves between hosts, then any data was present on the
    > instance store volume is lost

    -   if they are moved to a new host, the instances are given a new
        > blank ephemeral volumes

        -   the data on the previous volume is lost, as they are whipped
            > before they are re-assigned

    -   instances can move hosts for many reasons

        -   when they are stopped and started

        -   if the instance is resized

        -   if the host is in maintenance

        -   changing an instance type

        -   if the volume fails

> ![](media/image39.jpeg){width="0.16666666666666666in"
> height="0.14583333333333334in"}- they are temporary data holders

-   should not be used for persistent data

```{=html}
<!-- -->
```
-   some instance types do not support store volumes

-   as the instance increases in time, it has a large number of instance
    > store volumes

> ![](media/image39.jpeg){width="0.16666666666666666in"
> height="0.14583333333333334in"}- **advantages**

-   performance

-   high level of throughput

-   more IOPS

> ![](media/image39.jpeg){width="0.16666666666666666in"
> height="0.14583333333333334in"}- instance store volume **can be added
> only when the instance is launched**

AWS Developer Page 138

**Choosing Between the EC2 Instance Store and EBS**

+------------------------------------------------+---------------------+
| Sunday, July 25, 2021                          | > 3:40 PM           |
+================================================+=====================+
+------------------------------------------------+---------------------+

![](media/image221.png){width="7.321527777777778in"
height="5.188194444444444in"}

+---+---+--------------------------------+---+---------------------------------+---+
|   | > |                                | > |                                 |   |
|   |   |                                |   |                                 |   |
|   | E |                                | E |                                 |   |
|   | C |                                | l |                                 |   |
|   | 2 |                                | a |                                 |   |
|   | > |                                | s |                                 |   |
|   |   |                                | t |                                 |   |
|   | I |                                | i |                                 |   |
|   | n |                                | c |                                 |   |
|   | s |                                | > |                                 |   |
|   | t |                                |   |                                 |   |
|   | a |                                | B |                                 |   |
|   | n |                                | l |                                 |   |
|   | c |                                | o |                                 |   |
|   | e |                                | c |                                 |   |
|   | > |                                | k |                                 |   |
|   |   |                                | > |                                 |   |
|   | S |                                |   |                                 |   |
|   | t |                                | S |                                 |   |
|   | o |                                | t |                                 |   |
|   | r |                                | o |                                 |   |
|   | a |                                | r |                                 |   |
|   | g |                                | a |                                 |   |
|   | e |                                | g |                                 |   |
|   |   |                                | e |                                 |   |
+===+===+================================+===+=================================+===+
|   |   | > Temporary storage            |   | > Persistent Storage            |   |
+---+---+--------------------------------+---+---------------------------------+---+
|   |   |                                |   |                                 |   |
+---+---+--------------------------------+---+---------------------------------+---+
|   |   | > Data can be lost from:       |   | > \- service that is resilient  |   |
|   |   |                                |   | > in an AZ                      |   |
+---+---+--------------------------------+---+---------------------------------+---+
|   |   | > \- hardware failure          |   | > \- you can snapshot volumes   |   |
|   |   |                                |   | > on S3 which are               |   |
+---+---+--------------------------------+---+---------------------------------+---+
|   |   | > \- instance rebooting        |   | > region resilient              |   |
+---+---+--------------------------------+---+---------------------------------+---+

-   maintenance

-   anything that moves instances from a host to another

+---+--------------------------------+---+---------------------------------+---+
|   | > Volumes can be attached only |   | > The storage is isolated from  |   |
|   | > at the instance\'s launch    |   | > instance lifecycle            |   |
+===+================================+===+=================================+===+
|   |                                |   |                                 |   |
+---+--------------------------------+---+---------------------------------+---+
|   | > time                         |   | > \- attach and detached        |   |
|   |                                |   | > volumes at anytime            |   |
+---+--------------------------------+---+---------------------------------+---+
|   | > They are included in the     |   | > Cost efficiency but the       |   |
|   | > instance price               |   | > advantages of EBS are needed  |   |
|   |                                |   | > =                             |   |
+---+--------------------------------+---+---------------------------------+---+
|   |                                |   | > ST1 or SC1                    |   |
+---+--------------------------------+---+---------------------------------+---+
|   |                                |   | > Throughput or Streaming = ST1 |   |
+---+--------------------------------+---+---------------------------------+---+
|   |                                |   | > Boot cannot be used from ST1  |   |
|   |                                |   | > or SC1                        |   |
+---+--------------------------------+---+---------------------------------+---+
|   |                                |   |                                 |   |
+---+--------------------------------+---+---------------------------------+---+
|   |                                |   | > GP2/3the maximum possible     |   |
|   |                                |   | > performance is 16,000         |   |
+---+--------------------------------+---+---------------------------------+---+
|   |                                |   | > IOPS/volume                   |   |
+---+--------------------------------+---+---------------------------------+---+
|   |                                |   | > IO1 and IO2 can deliver up to |   |
|   |                                |   | > 64,000 IOPS                   |   |
+---+--------------------------------+---+---------------------------------+---+
|   |                                |   | > \- needs to be paired with an |   |
|   |                                |   | > EC2 instance that is          |   |
+---+--------------------------------+---+---------------------------------+---+
|   |                                |   | > capable to deliver such       |   |
|   |                                |   | > performance                   |   |
+---+--------------------------------+---+---------------------------------+---+
|   | > If temporary storage is an   |   | > You can take multiple EBS     |   |
|   | > option, then instance        |   | > volumes, and create a         |   |
|   |                                |   | > **RAID**                      |   |
+---+--------------------------------+---+---------------------------------+---+
|   | > volumes are a good choice as |   | > **0** set from those volumes  |   |
|   | > they can deliver more        |   |                                 |   |
+---+--------------------------------+---+---------------------------------+---+
|   | > than 260,000 IOPS            |   | > \- gets the performance of    |   |
|   |                                |   | > all the **volumes combined**  |   |
|   |                                |   | > -                             |   |
+---+--------------------------------+---+---------------------------------+---+
|   |                                |   | > up to 260,000 IOPS (maximum   |   |
|   |                                |   | > possible IOPs/instance)       |   |
+---+--------------------------------+---+---------------------------------+---+
|   |                                |   |                                 |   |
+---+--------------------------------+---+---------------------------------+---+

> AWS Developer Page 139

![](media/image222.png){width="7.497222222222222in"
height="10.002083333333333in"}

AWS Developer Page 140

**Snapshots, Restore & Fast Snapshot Restore (FSR)**

+------------------------------------------------+---------------------+
| Sunday, July 25, 2021                          | > 4:02 PM           |
+================================================+=====================+
+------------------------------------------------+---------------------+

> **Snapshots** provide few different functionalities:

-   to backup EBS volumes to S3

    -   useful to protect the data on those volumes against AZ issues or
        > local storage system failure in that AZ

-   can be used to migrate data from an EBS volume between different AZ
    > using S3 as an intermediatory

> **Snapshots** are essentially backups of EBS volumes which are
> **stored on S3.**

-   the data that the snapshot stores becomes region resilient (with EBS
    > was AZ resilient)

-   are increment in nature

    -   the first snapshot of a volume is a copy of all the data present
        > on the volume at that time

        -   copies this data from the volume to S3

    -   future snapshots are fully incremental

        -   they only store the difference between the previous snapshot
            > and the state of the volume at that moment

-   volumes can be created empty, or restored from a snapshot

    -   therefore snapshots are very useful to clone a volume

-   can be copied between AWS regions

-   are really flexible

> ![](media/image38.jpeg){width="0.16666666666666666in"
> height="0.16666666666666666in"}- When a new EBS volume is created,
> without using a snapshot, the performance is available immediately

-   there is no need for an initialization process

```{=html}
<!-- -->
```
-   When a volume is created and restores a snapshot it does the restore
    > lazily

    -   There are two restores available:

        1.  force a read of all data immediately - which forces EBS to
            > pull all the snapshot data from S3

        2.  immediate restore (Fast Snapshot Restore)

            -   you can create 50 immediate restore
                > snapshots/**region**, and when this feature is enabled
                > on a snapshot it requires to select the AZs that you
                > want to able to instant restore to

            -   they cost extra

-   are build using a gigabyte month metric

AWS Developer Page 141

**EBS Encryption (Theory & Demo)**

+------------------------------------------------+---------------------+
| Tuesday, July 27, 2021                         | > 2:50 PM           |
+================================================+=====================+
+------------------------------------------------+---------------------+

> By default there is no encryption to an EBS but the OS could perform
> encryption internally.
> ![](media/image104.jpeg){width="0.16666666666666666in"
> height="0.13541666666666666in"}○ but they can be set to encrypt by
> default using CMK

-   EBS encryption provides **at REST encryption** for volumes or
    > snapshots

-   it uses a **KMS key** - a customer or AWS a managed mater key

-   a data encryption key (DEK) is stored with the volume in an
    > encrypted form - can be decrypted using KMS

    -   when used, a decrypted version of the key is stored in **memory
        > only** and can be used to all encryption operations

-   when creating a snapshot the same DEK is used to encrypt the
    > snapshot

    -   when creating a volume from the snapshot the same key is used to
        > decrypt the

> data on the new volume
>
> ![](media/image38.jpeg){width="0.16666666666666666in"
> height="0.16666666666666666in"}○ each volume has **one unique DEK**
> and is inherited by its snapshot and volumes generated by snapshots
>
> ![](media/image104.jpeg){width="0.16666666666666666in"
> height="0.13541666666666666in"}○ once a volume is encrypted it cannot
> be set to be unencrypted

-   the **OS is not aware of the encryption** - the encryption happens
    > between the EC2 host and the EBS system - AES256

-   is free of charge - **but is has a CPU utilization**

AWS Developer Page 142

**Network Interfaces, Instance IPs and DNS**

+---------------------------------------------+------------------------+
| Friday, July 30, 2021                       | > 11:53 AM             |
+=============================================+========================+
+---------------------------------------------+------------------------+

> An EC2 instance always starts off with **one network interface (ENI -
> Elastic Network Interface)**.

-   optionally you can attach one or more ENI - but everything needs to
    > be in the same availability

> zone
>
> **Network interfaces**
>
> ![](media/image39.jpeg){width="0.16666666666666666in"
> height="0.14583333333333334in"}- have a MAC address - is the hardware
> address of the interface

-   has a primary IP version private address that is from the range of
    > the subnet

    -   can have 0 or more private address on the same interface

    -   can have zero or more public addresses on the same interface

    -   can have one ELASTIC IP ADDRESS/private IP address

        -   ELASTIC IP ADDRESSES are public IPv4 addresses - but are
            > different than public IPv4 addresses where there are one
            > per interface

    -   can have zero or more IPv6 - by default are publicly routable

    -   can have security groups which apply to network interfaces -
        > will impact all IP addresses on that interface

        -   security groups are attached to interfaces

    -   can enable/disable the source and destination check

    -   depending on the instance you can have different network
        > interfaces

        -   the capabilities of the second interfaces is the same as the
            > primary one

        -   except they can be detached and moved to other EC2 instances

            -   **private IP is fixed**

            -   **public IP is dynamic -** changes at stop and start of
                > the instance - won\'t

> change at restart
>
> ![](media/image38.jpeg){width="0.16666666666666666in"
> height="0.16666666666666666in"}^^ public IPv4 addresses are dynamic

-   elastic IP address is static

> ![](media/image38.jpeg){width="0.16666666666666666in"
> height="0.16666666666666666in"}○ **the public DNS inside the VPC will
> resolve internally to the primary private IP address**
> ![](media/image38.jpeg){width="0.16666666666666666in"
> height="0.16666666666666666in"}^▪^ **outside the VPC the DNS will
> resolve to the public IPv4 address of that instance**

-   elastic IP addresses are allocated per AWS account, and they can be
    > associated to a private IP either on the primary interface or the
    > secondary interface

    -   if associated with the primary IP address the normal non-elastic
        > IPv4 address is

> removed, and the elastic IP address becomes the public IP address of
> the instance ![](media/image104.jpeg){width="0.16666666666666666in"
> height="0.13541666666666666in"}○ we should use different interface and
> not different IPs because of security groups which
>
> are attached to interfaces

![](media/image38.jpeg){width="0.16666666666666666in"
height="0.16666666666666666in"}

> ○ the OS never sees the IPv4 public address

AWS Developer Page 143

**Amazon Machine Images (AMI)**

+-----------------------------------------------+----------------------+
| Friday, July 30, 2021                         | > 3:05 PM            |
+===============================================+======================+
+-----------------------------------------------+----------------------+

> **AMI** are images of EC2.

-   a template configuration that can be used to create instances

-   can be used to launch EC2 instances

    -   AWS, Community or Marketplace provided

-   **AMI are regional resilient**

    -   can be used only in the region that is in

-   has a unique ID

> ![](media/image39.jpeg){width="0.16666666666666666in"
> height="0.14583333333333334in"}- AMI control permissions

-   by default only the account that creates it can use it

-   AMI can pe public

-   specific AWS account can accessit

```{=html}
<!-- -->
```
-   an AMI can be used to create an instance

-   an AMI can be created of an existing EC2 instance - capture the
    > current configuration of that instance

> AMI Lifecycle

-   has 4 phases

> **1. Launch**

-   used to launch an EC2 instance

> **2. Configure**

-   custom configuration of a launched EC2 instance

    -   certain OS with application or services installed

    -   certain set of volumes attached of a certain size

    -   an instance with a full application suite installed and
        > configured

    -   etc.

3.  **Create image**

    -   a copy (an AMI) of the instance and its volumes that are
        > attached to that instance

    -   it contains:

        -   permissions

        -   AMI ID

        -   snapshots of the EBS volumes attached

4.  **Launch**

    -   when the AMI (from step 3) is used to launch an instance

        -   will have the same volume configuration as the original

![](media/image223.jpeg){width="6.559027777777778in" height="2.96875in"}

> AWS Developer Page 144

![](media/image224.png){width="6.761805555555555in"
height="10.011111111111111in"}

> **AMI itself does not contain any real data volume**

![](media/image38.jpeg){width="0.16666666666666666in"
height="0.16666666666666666in"}

> **AMI is a container that references snapshots that are created from
> original EBS volumes**
>
> **together with the original device IDs**

![](media/image38.jpeg){width="0.16666666666666666in"
height="0.16666666666666666in"}

> **AMI are in one region**

![](media/image38.jpeg){width="0.16666666666666666in"
height="0.16666666666666666in"}

> **AMI backing** is a saying that refers to a configured instance that
> is then used to create an image of that instance

![](media/image38.jpeg){width="0.16666666666666666in"
height="0.16666666666666666in"}

> **AMI cannot be edited**

![](media/image38.jpeg){width="0.16666666666666666in"
height="0.16666666666666666in"}

> **AMIs can be copied across regions**

-   **remember that once a AMI has been copied to another region they
    > are two completely different AMIs**

AWS Developer Page 145

**EC2 Purchase Options - Launch Types**

+-------------------------------------------------+--------------------+
| Saturday, July 31, 2021                         | > 1:52 PM          |
+=================================================+====================+
+-------------------------------------------------+--------------------+

> On-Demand Purchase Option

-   is the default as is in the average of anything

-   instances are isolated from one another but multiple customer
    > instances can **share** hardware

-   instances of different sizes can run on the same EC2 hosts - each
    > consuming dined allocation resources

-   they are billed/second when they are running

-   storage is charged constantly no matter if the instance is running
    > or not

> When to use it

-   start your evaluation from this option and move to another if is
    > needed

-   there are no interruptions

    -   when launched, the instance is billed per second

    -   if the host is not failing there are no interruptions

    -   offers predicable prices

    -   no discounts

        -   therefore for short-term or unknown durations this option
            > should be used

> Sport Purchase Option

-   is the cheapest way to get access to EC2 capacity

-   selling unused EC2 host capacity for up to 90% discount

    -   the price is based on the spare capacity at a given time

-   the AWS account that needs an instance makes a max offer for the
    > SPOT

    -   regardless of the offer, they pay the price of the SPOT

-   when AWS increase price, instances which whom offers were lowers
    > than the new price are terminated

-   they are not **reliable**

> ![](media/image95.jpeg){width="0.16527777777777777in"
> height="0.14583333333333334in"}- should never be used for instances
> that cannot tolerate interruptions

-   should be used for:

    -   non time critical tasks

    -   anything that can be rerun

    -   if bursty capacity is needed

    -   cost sensitive workloads

    -   anything which is stateless

> Reserved Purchase Option

-   is for long term, consistent usage of EC2

-   is a commitment made to AWS that you will use these resources for
    > these amount of time, therefore they are cheaper

    -   but you are billed no matter if you use the resources or not

    -   you can commit for 1 year or 3 years

        -   no-upfront payment option which reduces the per second fee -
            > is paid even the instance is running or not

        -   all-upfront payment option means no per second fee at all

        -   partial-upfront payment options means that a part of the
            > payment is made in advance in exchange for lower per
            > second cost

![](media/image225.jpeg){width="7.125694444444444in"
height="1.1090277777777777in"}

> AWS Developer Page 146

![](media/image226.png){width="7.327083333333333in"
height="10.002083333333333in"}

-   matching instance, that has reduced or no charge/second

-   when you reserve a host for an EC2 instance, if there are extra
    > resources not used - they are still billed

-   they can be purchased for a particular type of instance

    -   they can be locked to an AZ or to a region

        -   for AZ reservation - you can benefit only if you launch
            > instances in that AZ and it does reserves capacity

        -   for a region reservation - it does not reserve capacity but
            > it can benefit the instances that are launched into any AZ
            > of that region

-   can have a partial effect

    -   if you reserve not enough resources for the instance - this
        > reservation will have partial coverage

-   they are good for:

    -   for components of the infrastructure that have known usage

    -   require consistent access to compute

    -   required for long term

> Scheduled Reserved Instances

-   they are great for **long-term requirements which do not run
    > constantly**

-   a **scheduled reserved instance is a commitment** - the frequency
    > and times for running needs to be specified

    -   you get the required capacity for a slightly cheaper rate versus
        > on demand

-   it does not support all instance types of regions

-   minimum 1200 hours/year

-   1 minimum year

-   **very good for long term usage, but when not the full time period
    > is needed**

> Capacity Reservations

-   In case of emergency situations such a major failures, there might
    > not be enough capacity within a region or an availability zone

    -   in that situation there is **an order to things - a priority
        > order which AWS use to deliver EC2 capacity**

-   **priorities:**

    1.  AWS delivers the commitments in terms of **reserved purchases**

    2.  AWS delivers **on-demand resources**

    3.  AWS delivers any leftover capacity to the **spot purchased**

```{=html}
<!-- -->
```
-   Capacity reservation is different than reserved instance

    -   has 2 components - capacity and billing component

```{=html}
<!-- -->
```
-   **Regional reservation** provides billing discount for valid
    > instances launched in any AZ in that region

    -   they do not reserve capacity within an AZ, which is risky during
        > major faults when capacity is limited

> AWS Developer Page 147

-   zonal reservation give you the same billing discount as using
    > regional reservations but they reserve capacity in a specific AZ

-   you need to commit for 1 or 3 years term with AWS

```{=html}
<!-- -->
```
-   **On-demand capacity reservations** can be booked to ensure you
    > always have access to capacity in an AZ when you needed it **but
    > at full on demand price**

    -   no term limits

> Saving plan

-   hourly commitment for 1 or 3 years term

-   come in two main types

    1.  general compute amounts

    2.  EC2 Savings Plan - flexibility on size and OS

-   compute products have an on-demand rate, and a savings rate

-   when the hour commitment is reached - on demand is used

> ![](media/image92.jpeg){width="0.16527777777777777in"
> height="0.16527777777777777in"}- this option could allow organizations
> migrating from EC2 instances to emerging architectures (serverless
> arhitectures) to get cost effective access to resources

![](media/image227.jpeg){width="6.950694444444444in"
height="3.3541666666666665in"}

> Dedicated Hosts Purchase Option

-   is an EC2 host which is allocated to you **entirely**

-   the host itself is billed - instances are not charged

-   they come with all the resources that you would expect from a
    > physical machine

-   offers the licensing based on sockets/cores

-   has a feature called **host affinity** which links an instance to a
    > host, and the instance never changes the host

> Dedicated Instances Purchase Option

-   you do not share host with anyone else

-   but you do not own the host

-   it comes with extra fees:

    -   one-off hourly fee for any regions where the dedicated instances
        > are used

    -   there is a fee for each dedicated instance

> AWS Developer Page 148

AWS Developer Page 149

**Instance Status Checks & Auto Recovery**

+-------------------------------------------------+--------------------+
| Sunday, August 1, 2021                          | > 7:47 PM          |
+=================================================+====================+
+-------------------------------------------------+--------------------+

> Every EC2 instance has two high level/instance status checks:

-   if both checks pass that means that all is well with the instance

-   each checks represents a separate set of tests

> The checks are:

1.  checks the system status

    -   a failure here could indicate:

        -   loss of system power

        -   loss of network connectivity

        -   host hardware issues

        -   host software issues

    -   this tests are focused on the EC2 host or EC2 service

2.  checks the instant status

    -   a failure here could indicate:

        -   corrupt file system

        -   incorrect networking

        -   OS or Kernel issues

    -   focuses on instances

> Anything that the two checks passed, represents an issue that needs to
> be resolved, by the following:

-   you can stop and start an instance

-   restart an instance

-   terminate and recreate

-   ask EC2 instance to perform an auto recovery

    -   requires to have spare EC2 capacity

    -   a recovered instance is identical to the original instance,
        > including the instance ID, private IP addresses, Elastic IP
        > addresses, and all instance metadata

    -   terminated instances cannot be recovered

AWS Developer Page 150

**Horizontal & Vertical Scaling**

+--------------------------------------------------+-------------------+
| Monday, August 2, 2021                           | > 1:06 PM         |
+==================================================+===================+
+--------------------------------------------------+-------------------+

> Horizontal and Vertical scaling are two different ways a system can
> scale to handle increasing or decreasing load placed on that system.
>
> **Scaling** is what happens when a system needs to grow or shrink in
> response to increases or decreases of loads placed upon the system by
> tis customers. Basically, adding or removing resources from the
> system.

+----------------------------------+-----------------------------------+
| > **Horizontal**                 | > **Vertical**                    |
+==================================+===================================+
| > adds more instances, instead   | > resizing an EC2 instance when   |
| > of changing the instance       | > scaling                         |
+----------------------------------+-----------------------------------+
| > size                           | > \- requires a restart -         |
|                                  | > interruption                    |
+----------------------------------+-----------------------------------+
| > \- adds additional capacity    | > \- larger instance charge a     |
|                                  | > premium charge                  |
+----------------------------------+-----------------------------------+
| > \- instead of having one copy  | > \- has a cap - a limit of the   |
| > of the application,            | > upper size                      |
+----------------------------------+-----------------------------------+
| > which is scale more copies of  | > \- can change the size in       |
| > the application are            | > certain time windows            |
+----------------------------------+-----------------------------------+
| > made                           |                                   |
+----------------------------------+-----------------------------------+
| > \- each instance takes its     |                                   |
| > load on the incoming           |                                   |
+----------------------------------+-----------------------------------+
| > traffic                        |                                   |
+----------------------------------+-----------------------------------+
| > ○ requires a **load balances** |                                   |
| > which is an                    |                                   |
+----------------------------------+-----------------------------------+
| > appliance which sits between   |                                   |
| > the servers                    |                                   |
+----------------------------------+-----------------------------------+
| > and customers                  |                                   |
+----------------------------------+-----------------------------------+
| > ○ the load balancer            |                                   |
| > distributes the load to all    |                                   |
+----------------------------------+-----------------------------------+
| > the instances running          |                                   |
+----------------------------------+-----------------------------------+
| > sessions do not work with      | > works for all applications even |
| > horizontal scaling             | > monolithic ones                 |
+----------------------------------+-----------------------------------+
| > \- because the user might use  |                                   |
| > a different instance           |                                   |
+----------------------------------+-----------------------------------+
| > for different functionalities  |                                   |
+----------------------------------+-----------------------------------+
| > \- therefore, requires         |                                   |
| > application support or         |                                   |
| > off-host                       |                                   |
+----------------------------------+-----------------------------------+
| > sessions                       |                                   |
+----------------------------------+-----------------------------------+
| > \- in **off-session hosts**    |                                   |
| > the session details are stored |                                   |
+----------------------------------+-----------------------------------+
| > in another place (database) so |                                   |
| > the servers are                |                                   |
+----------------------------------+-----------------------------------+
| > stateless                      |                                   |
+----------------------------------+-----------------------------------+
| > **no disruptions** while       | > no modifications are required   |
| > scaling                        | > for the application             |
+----------------------------------+-----------------------------------+
| > \- existing instances are not  |                                   |
| > being impacted                 |                                   |
+----------------------------------+-----------------------------------+
| > there are **no limits** to     |                                   |
| > this type of scaling           |                                   |
+----------------------------------+-----------------------------------+
| > is **less expensive**          |                                   |
+----------------------------------+-----------------------------------+
| > allows you to be more          |                                   |
| > **granular** in how you scale  |                                   |
+----------------------------------+-----------------------------------+
|                                  |                                   |
+----------------------------------+-----------------------------------+

> AWS Developer Page 151

![](media/image228.png){width="7.366666666666666in"
height="10.002083333333333in"}

AWS Developer Page 152

**Instance Metadata**

+-------------------------------------------------+--------------------+
| Monday, August 2, 2021                          | > 1:41 PM          |
+=================================================+====================+
+-------------------------------------------------+--------------------+

> The EC2 instance **metadata** is a service that EX2 provides to
> instances

![](media/image38.jpeg){width="0.16666666666666666in"
height="0.16666666666666666in"}

> ○ is data about the instance that is used to configure or manage a
> running instance

![](media/image38.jpeg){width="0.16666666666666666in"
height="0.16666666666666666in"}

> ○ a way that the instance or anything running inside the instance can
> access information about the environment
>
> ![](media/image229.png){width="0.3333333333333333in"
> height="0.14583333333333334in"}○ the IP address to access the metadata
> is **169.254.169.254**/latest/meta-data/

-   The information about the environment is divided by categories

    -   hostname

    -   events

    -   security groups

    -   networking

![](media/image38.jpeg){width="0.16666666666666666in"
height="0.16666666666666666in"}

> ○ it has no authentication

![](media/image38.jpeg){width="0.16666666666666666in"
height="0.16666666666666666in"}

> ○ is not encrypted

-   anyone who can access the instance\'s command shell can access the
    > meta-data

AWS Developer Page 153

**Bootstrapping**

+--------------------------------------------------+-------------------+
| Monday, August 16, 2021                          | > 3:23 PM         |
+==================================================+===================+
+--------------------------------------------------+-------------------+

> **Bootstrapping** allows adding automation to the solutions designed.

-   is process where script and other configurations can be run when an
    > **instance is first launched**

-   an instance can be brough into service in a pre-configured state

-   it exists outside EC2

-   allows a system to self-configure or perform some configuration
    > steps

-   in **EC2** allows for build automation

-   is enabled using EC2 user data and this is injected into the
    > instance in the same way that metadata is

    -   is accessed using the meta-data IP address
        > **165.254.165.254/latest/user-data**

    -   everything passed in is executed bu the instance\'s OS

    -   it is executed **only once on launch time**

    -   does not validate the data before executing it

-   the user data is **not secure**, for the instance is just a block of
    > data ![](media/image216.jpeg){width="0.16666666666666666in"
    > height="0.13541666666666666in"}○ long term credentials should not
    > be passed in

-   the user data is limited to **16KB** in size

    -   for anything larger than that a script is required which would
        > download the necessary data

-   user data can be modified if you shut down the instance

-   with **AMI** the service time is measured in minutes

![](media/image230.jpeg){width="6.511111111111111in"
height="2.9590277777777776in"}

> Architecture

-   once an instance is created from scratch or from an AMI, it looks
    > for any user data

-   if the user-data exists it executes it at launch time

    -   if the execution is **successful** then the instance will be
        > running - functional

    -   if the execution is **not successful** then the instance will be
        > in a running state , but the instance will not be configured
        > as intended

AWS Developer Page 154

**EC2 Instance Roles & Profile**

+--------------------------------------------------+-------------------+
| Monday, August 16, 2021                          | > 6:48 PM         |
+==================================================+===================+
+--------------------------------------------------+-------------------+

> Instance Roles
>
> Everything starts with an IAM role, role which has permissions
> attached to it.

-   whomever assumes the role has temporary credentials and given
    > permissions

-   and EC2 instance role allows an EC2 instance to assume a role

-   the application running inside the instance can use the permissions
    > that the role provides

-   an **InstanceProfile** is a wrapper around the IAM role

    -   allows the permissions to get inside the instance

    -   the role is not attached to the instance, is the InstanceProfile
        > that is attached to the

> instance
>
> ![](media/image38.jpeg){width="0.16666666666666666in"
> height="0.16666666666666666in"}- temporary credentials are delivered
> to an instance via the **instance meta-data**
> ![](media/image104.jpeg){width="0.16666666666666666in"
> height="0.13541666666666666in"}○ the credentials inside the instance
> meta-data are always valid

-   they are renewed before they expire

> ![](media/image104.jpeg){width="0.16666666666666666in"
> height="0.13541666666666666in"}-
> iam/security-credentials/**role-name**
>
> ![](media/image39.jpeg){width="0.16666666666666666in"
> height="0.14583333333333334in"}- **you should always use roles rather
> than adding access keys to an instance**

AWS Developer Page 155

**Cloud Formation**

+------------------------------------------------+---------------------+
| Thursday, June 17, 2021                        | > 12:30 PM          |
+================================================+=====================+
+------------------------------------------------+---------------------+

> **Cloud formation** is a tool that allows you to create, update and
> delete infrastructure in a AWS account.
>
> Instead of deleting and creating resources manually, a template can be
> created.
>
> The **CloudFormation** automates infrastructure
>
> A cloud formation template is written in **YAML** or **JSON**.
>
> **Templates have:**

-   a list of **resources**

    -   **the only mandatory part**

-   description

    -   lets the author to add a description

    -   it is usually used to describe what the template does, its
        > resources, cost of the template etc.

    -   the description needs to follow directly after the AWS template
        > format version!

-   metadata

    -   controls how different components are presented through the
        > console UI

    -   force how the UI presents the template

-   parameters

    -   fields that prompt the user for more information

-   mappings

    -   allows to create lookup tables

-   conditions

    -   actions that occur only if a condition is bet

-   outputs

    -   once the template is finished it will present outputs of what
        > had been created, updated or deleted

> **A template contains a logical stack of resources. When a template is
> executed, the Cloud formation creates a corresponding physical
> resource.**
>
> **A CloudFormation Physical resource is a physical resource by
> creating a CloudFormation stack**

AWS Developer Page 156

**Shared Responsibility Model**

+-------------------------------------------------+--------------------+
| Tuesday, June 22, 2021                          | > 1:59 PM          |
+=================================================+====================+
+-------------------------------------------------+--------------------+

> **Shared Responsibility Model**

![](media/image231.jpeg){width="7.4527777777777775in"
height="3.527083333333333in"}

> AWS Developer Page 157

**High-Availability vs Fault-Tolerance vs Disaster Recovery**

+-------------------------------------------------+--------------------+
| Tuesday, June 22, 2021                          | > 3:06 PM          |
+=================================================+====================+
+-------------------------------------------------+--------------------+

> High-Availability (HA)
>
> **Maximize uptime**

-   aims to ensure an **agreed level of operational performance**
    > usually uptime, for a higher than normal period

-   -designed to be online as much as possible

-   is not about the user experience

-   is about maximizing the online time as much as possible

-   this required backup (redundant) system to replace of a outbreak
    > system

    -   this action has a small outbreak time, and this is okey

> Fault-Tolerance (FT)
>
> **Operating through failure**

-   is the property that enables a system to continue operating properly
    > in the event of the failure of some or more components

-   if a system has faults, it should continue properly until the faults
    > are fixed

-   system are designed to work through failure without disruption

> Disaster Recovery (DR)
>
> **Keep the crucial and non-replaceable parts of the system safe**

-   **what we do when high-availability and fault-tolerance DO NO WORK**

-   a set of policies, tools and procedures to enable the recovery or
    > the continuation of vital technology infrastructure and systems,
    > following a natural or human-induced disaster

-   plan for an action plan when disaster occur

-   is a multiple steps processes:

    -   what happens before (pre-planning)

        -   backup premises

        -   virtual backup systems

        -   offsite backup storage

        -   DR testing

    -   what happens after (disaster recovery process)

AWS Developer Page 158

**DNS**

+-------------------------------------------------+--------------------+
| Tuesday, June 22, 2021                          | > 3:40 PM          |
+=================================================+====================+
+-------------------------------------------------+--------------------+

> **DNS** is a **discovery service**, it helps users to discover system
> on the internet.
>
> **DNS is resilient, distributed and scalable.**

-   it translates information machine into human and vice-versa

-   translate a domain name to an IP address

-   is huge, resilient and hard to distribute

-   is a database, distributed and global

-   each server has a ZONE file, that links a domain name to the correct
    > IP address

    -   that zone file is located anywhere on potentially one or two of
        > millions of DNS name services.

    -   the DNS resolver is sitting either on the internet router, or
        > the provider

![](media/image232.jpeg){width="4.017361111111111in"
height="1.6902777777777778in"}

> **DNS** is distributed, the data is stored in zone files, and the zone
> files are stored on name servers globally.
>
> The DNS needs a start point.
>
> **DNS flow:** The DNS resolver needs to locate the correct name server
> for a given zone, query that name
>
> server and retrieve the information it needs, and then pass it back to
> the DNS client.
>
> The DNS is structured as a tree. The DNS root (domain name), is stored
> on 13 special servicer known as
>
> **DNS root servers**. This servers are the entry point.

![](media/image233.jpeg){width="3.907638888888889in"
height="1.8604166666666666in"}

> 1\. The DNS client asks a DNS resolver of given DNS name
>
> 2\. using the root hints file, the DNS resolver communicated with one
> or more root servers to access the root zone and begin the process of
> finding the IP address
>
> A local system (laptop, desktop, etc.). The local system will use a
> **DNS resolver server** which is located on
>
> the local router or internet provider. The vendor of the OS (Microsoft
> for Windows, OS maintaining
>
> group for Linux, etc.) supply the root hints file. The **root hints
> file** is a pointer to the DNS root servers.
>
> **Top level domains** are in the root zone (.com, .org, .uk, etc.).
> This root zone database is managed the
>
> IANA. These root zones point to other servers that manages country
> codes zones.

![](media/image234.jpeg){width="3.8826388888888888in"
height="1.8833333333333333in"}

> The image above is how the chain of trust works in DNS.
>
> AWS Developer Page 159

![](media/image235.png){width="4.043055555555555in"
height="10.002083333333333in"}

> AWS Developer Page 160

**Route 53**

+---------------------------------------------------+------------------+
| Wednesday, June 23, 2021                          | > 2:53 PM        |
+===================================================+==================+
+---------------------------------------------------+------------------+

> Route 53 provides to main services:

1.  Register domains

2.  Host zone files and manage nameservers

> Route53 is a global service with a single database, and it is globally
> resilient.
>
> Register domains
>
> Route 53 allows the registration of domains, and to do that it has
> relationships with major domain registers.
>
> When registering a domain Route 53 follows the following steps:

1.  registers a zone file (dora.org)

2.  allocates a name service for that zone

3.  puts the zone file in 4 name servers

4.  communicates to .org registry to add the new domain into the zone
    > file for the.org top level domain

> a\. using name server records
>
> Host zone
>
> (DNS as a service)
>
> This service allows hosting, creating and managing zone files.
>
> Zone files are hosted on 4 managed name servers.
>
> When a hosted zone is created , a number of server are allocated and
> linked to the hosted zone.
>
> A hosted zone can be public (accessible on the public internet) or
> private which means that they are linked to one or more VPCs.

AWS Developer Page 161

**DNS Record Types**

+---------------------------------------------------+------------------+
| Wednesday, June 23, 2021                          | > 4:02 PM        |
+===================================================+==================+
+---------------------------------------------------+------------------+

> Which type of organisation maintains the zones for a TLD
>
> Registry
>
> Which type of organisation has relationships with the .org TLD zone
> manager allowing domain registration?
>
> Registrar
>
> Nameserver (NS)
>
> Nameservers are record types, which allow delegation to occur in DNS

![](media/image236.jpeg){width="6.339583333333334in" height="2.8375in"}

> **NS record - delegates control of .org to the .org registery**
>
> **A record - \> IPv4 addresses**
>
> **AAAA record -\> IPv6 addresses**
>
> **CNAME record -\> Cnames cannot point directly at an IP address, only
> at other names.**
>
> AWS Developer Page 162

![](media/image237.png){width="6.552083333333333in"
height="10.002083333333333in"}

> **MX Records - are used as apart of a process (mail)**

![](media/image238.jpeg){width="6.236111111111111in"
height="3.035416666666667in"}

> **TXT Records - add arbitrary text to a domain - is used to prove
> ownership**

AWS Developer Page 163

![](media/image239.png){width="6.441666666666666in"
height="10.002083333333333in"}

> **DNS TTL - Time to live**
>
> ATTL value is set to DNS record, is a numeric value in seconds.
>
> Walking the tree takes time, to talk with the root, and all the
> following levels to get the result needed. It is a lengthy processes.
>
> The TTL specifies for how long the response values can be cached. This
> is set by the administrator. Once a request had been responded to, and
> the result is cached on the resolver server, other clients do not need
> to wait too much for a response.
>
> Authoritative and non-authoritative responses are the same, so in this
> case TTL matters when things change so that responses are not delayed
> (if TTL is high).

When things change, the TTL must be changed to a low value, or have a
low value of TTL all the time.

AWS Developer Page 164

**Introduction to Containers**

+--------------------------------------------------+-------------------+
| Wednesday, August 11, 2021                       | > 12:35 PM        |
+==================================================+===================+
+--------------------------------------------------+-------------------+

> **Virtualization** - running multiple OS on the same hardware

![](media/image240.jpeg){width="4.600694444444445in" height="1.91875in"}

> A **container** is similar to a virtual machine, in many ways, because
> it provides an isolated environment which an application can run
> within.
>
> ![](media/image241.jpeg){width="0.12986111111111112in"
> height="0.10416666666666667in"} Virtual machines run a whole isolated
> OS on top of a host OS, a container runs as a process within the host
> OS A **container** is a process

-   isolated from all the other processes

-   it can use the host OS for many things

    -   networking

    -   file I/O

-   the process acts like its own OS

    -   has its own file system

    -   can run child processes inside it

-   the OS can run multiple containers at the same time, each isolated
    > from each other

-   is much lighter than virtual machines allowing way more containers
    > to exist than virtual machines could on the same OS

-   

![](media/image242.jpeg){width="4.9375in" height="2.567361111111111in"}

> \-
>
> Container anatomy
>
> A container is a running copy of a **Docker Image.**

-   **the images are made of multiple independent layers**

    -   they are not a single monomythic image

    -   they are created by using a docker file

![](media/image243.jpeg){width="4.354166666666667in"
height="1.8222222222222222in"}

> ► **base image of centos7**

► **performs updates and installs the webserver**

> ► **adds a script to the image**
>
> AWS Developer Page 165

![](media/image244.png){width="5.1in" height="10.009722222222223in"}

> ► **adds a script to the image**

-   each line in a docker file is processed one by one and each line
    > creates a new file system layer inside the Docker Image it creates

```{=html}
<!-- -->
```
-   each Docker Image are created from scratch or by using another
    > Docker Image

![](media/image245.jpeg){width="4.352083333333334in"
height="2.063888888888889in"}

> \-

-   is a stack, so the **green** layer is on top!

A **docker** image is how we create a Docker Container

-   is a running copy of an image with one difference

    -   

    -   has an additional **read/write** file system layer

    -   images are **read only**

-   an image can be used to create **multiple** containers

![](media/image246.jpeg){width="3.4006944444444445in"
height="0.9465277777777777in"}![](media/image247.jpeg){width="2.2819444444444446in"
height="1.7416666666666667in"}

> ○

-   **all the layers are the same,** besides the read/write containers -
    > they do not overlap - they are isolated

-   containers will differ few megabytes because of the read/write layer

    -   the rest is reused between the containers

    -   because of this scales really well

```{=html}
<!-- -->
```
-   a **container registry** - docker hub

    -   is a registry or a hub of container images

    -   docker hosts can run many containers based on one or more images

    -   a single image can be used to generate containers on many
        > different Docker Hosts

    -   the docker hub can be used to download container images, or to
        > upload your own

        -   private registries can require authentication

![](media/image248.jpeg){width="3.1284722222222223in"
height="1.36875in"}![](media/image249.jpeg){width="3.1284722222222223in"
height="1.36875in"}

> ○
>
> AWS Developer Page 166

![](media/image250.png){width="3.875in" height="10.002083333333333in"}

> ○

Key Concepts

-   dockers file are used to build docker images

-   docker images are multi-layered file system images which are used to
    > **run** containers

-   containers are a great tool as they are portable, self-contained and
    > always run as expected

-   containers and images are super light weight

    -   they use the host OS for the heavy lifting but they are isolated

-   images can be based on other images

-   layers are **read only**

-   **an images is a set of layers grouped together** which can be
    > shared and reused

-   containers only run what is needed

    -   they use very little memory

    -   they are very fast

-   provides the same isolation as virtual machines

-   they need ports to be connected with the outside world

> AWS Developer Page 167

**Elastic Container Service - ECS - Concepts**

+----------------------------------------------------+-----------------+
| Wednesday, August 11, 2021                         | > 2:16 PM       |
+====================================================+=================+
+----------------------------------------------------+-----------------+

> **ECS** is a product that allows you to use containers running on
> infrastructure which AWS fully manage and partially manage

-   it takes away much of the admin overhead of self-managing the
    > container hosts

-   ECS is to containers what EC2 is to virtual machines

-   ECS uses clusters which run in one of two modes

    -   **EC2 mode** which uses EC2 instances as container hosts

    -   **fargate mode** which is a serverless way of running docker
        > containers where AWS manage the container host part and just
        > leave you to define an architect to your environment using
        > containers

-   ECS is a service that accept containers and instructions that you
    > provide

    -   it orchestrates where and how to run containers

    -   it is a managed container based compute service

    -   allows you to create a cluster

        -   **clusters are where containers run from**

    -   containers are **all based on container images**

    -   the container images need to be located on a container registry
        > somewhere (e.g. docker hub)

        -   AWS provides a registry called Elastic Container Registry
            > (ECR)

            -   it is integrated in AWS

    -   to allows ECS to know where the container images are a
        > **container definition** is needed

> ![](media/image38.jpeg){width="0.16666666666666666in"
> height="0.16666666666666666in"}^▪^ the container definition tells ECS
> where the container images is
>
> ![](media/image38.jpeg){width="0.16666666666666666in"
> height="0.16666666666666666in"}^▪^ tells ECS which port the container
> uses

-   provides the information about the single container that needs to be
    > defined

```{=html}
<!-- -->
```
-   a **task definition** in ECS represents a self-contained application

    -   can have one or more containers defined inside

    -   represents the application as a hole and it stores whatever the
        > container

> definitions were used to make up the single application
>
> ![](media/image38.jpeg){width="0.16666666666666666in"
> height="0.16666666666666666in"}^▪^ stores the resources used by the
> task: CPU, memory, networking mode, compatibility mode, and the **task
> role** (an IAM role that a task can assume)
>
> ![](media/image38.jpeg){width="0.16666666666666666in"
> height="0.16666666666666666in"}□ when a task assumes a role it gains
> temporary credentials which can be used within the task
>
> ![](media/image38.jpeg){width="0.16666666666666666in"
> height="0.16666666666666666in"}□ are the best practice way of giving
> permissions to access AWS products and services to containers within
> ECS
>
> ![](media/image38.jpeg){width="0.16666666666666666in"
> height="0.16666666666666666in"}○ a **service definition** defines a
> service. A service is how for ECS can define how a task can scale, how
> many copies can run

-   it can add capacity and resilience

-   used to provide a level of scalability and high availability

-   used how replacing failed tasks are managed

-   used to distribute load across multiple copies of the same task

AWS Developer Page 168

**ECS - Cluster Mode**

+----------------------------------------------------+-----------------+
| Wednesday, August 11, 2021                         | > 3:31 PM       |
+====================================================+=================+
+----------------------------------------------------+-----------------+

> EC2 Mode
>
> ECS management components:

-   handles high level tasks such as scheduling, orchestration, cluster
    > management and the

> placement engine which handles where to run containers - they exists
> in both modes

![](media/image38.jpeg){width="0.16666666666666666in"
height="0.16666666666666666in"}

-   and ECS cluster is created within a VPC inside the AWS account

    -   it benefits from the multiple AZ which are available within the
        > VPC

-   when creating a container the initial size needs to be specified

    -   it controls the number of container instances

    -   handled by Auto Scaling Group - used for horizontal scale in EC2
        > instances - adding and removing instances as required

-   you are responsible for the EC2 instances that are acting as
    > container hosts

    -   the capacity and the availability of the cluster needs to be
        > managed by you

-   uses container registry - where the images are stored

> ![](media/image38.jpeg){width="0.16666666666666666in"
> height="0.16666666666666666in"}- should be used if containers are
> needed and you need to manage the capacity, availability and other
> options
>
> Fargate Mode

-   EC2 instances do not need to be managed

-   there are no services needed to be managed by you

-   you are not paying for EC2 instances

-   handles high level tasks such as scheduling, orchestration, cluster
    > management and the placement engine which handles where to run
    > containers

-   uses container registry - where the images are stored

-   they use task and service definitions to define tasks and services

-   containers are hosted differently

    -   AWS maintains a shared Fargate infrastructure platform

    -   this platform is offered to all users of Fargate, with isolated
        > users

    -   resources are from a shared pool but there is no visibility of
        > other customers

    -   tasks and service definitions are shared

    -   a cluster uses a VPC which operates in AZs

    -   the allocated resources are injected into the used VPC from the
        > shared infrastructure

        -   each task is injected into the VPC and gets an Elastic
            > Network Interface

        -   at this point they work as any other VPC service

        -   they inherit the VPC setting - subnets, public IP, private
            > IP, etc.

-   you only pay for the containers used, because they come from the
    > shared infrastructure

    -   billing based on the resources that they consume

-   hosts do not need to managed, or manage capacity and availability

> Remember

1.  if you use containers use ECS

2.  containers make sense if you need to isolate your applications

    a.  which have low usage levels

    b.  which all use the same OS

    c.  when you do not need the overhead of virtualization

3.  you choose EC2 mode when you have a **large overload** and the
    > business is **price conscious**

4.  you choose Fargate for **large workload** and you need **less
    > management overhead**

5.  you choose Fargate for **small workload** because you only pay what
    > you use within the

AWS Developer Page 169

> container

6.  you choose Fargate for **batch** or **periodic workloads**

AWS Developer Page 170

**Exam guide**

+-----------------------------------------------+----------------------+
| Thursday, June 3, 2021                        | > 12:25 PM           |
+===============================================+======================+
+-----------------------------------------------+----------------------+

> AWS Developer Page 171

![](media/image251.png){width="7.622916666666667in"
height="10.002083333333333in"}

> AWS Developer Page 172

![](media/image252.png){width="7.622916666666667in"
height="10.002083333333333in"}

> AWS Developer Page 173

![](media/image253.png){width="7.622916666666667in"
height="10.002083333333333in"}

> AWS Developer Page 174
