


.. contents::
   :local:


admin-group relationship(admin_app.models.ADMIN_groups)
-------------------------------------------------------

::

 ADMIN_groups(id, admin, group)

.. list-table::
   :header-rows: 1

   * - Fullname
     - Name
     - Type
     - PK
     - Unique
     - Index
     - Null/Blank
     - Comment
   * - ID
     - id
     - bigint AUTO_INCREMENT
     - True
     - True
     - 
     - Blank
     - 
   * - admin
     - admin
     - bigint
     - 
     - 
     - True
     - 
     - FK:admin_app.models.ADMIN
   * - group
     - group
     - integer
     - 
     - 
     - True
     - 
     - FK:django.contrib.auth.models.Group


Options::

 unique_together : (('admin', 'group'),)
 default_permissions : ('add', 'change', 'delete', 'view')


admin-permission relationship(admin_app.models.ADMIN_user_permissions)
----------------------------------------------------------------------

::

 ADMIN_user_permissions(id, admin, permission)

.. list-table::
   :header-rows: 1

   * - Fullname
     - Name
     - Type
     - PK
     - Unique
     - Index
     - Null/Blank
     - Comment
   * - ID
     - id
     - bigint AUTO_INCREMENT
     - True
     - True
     - 
     - Blank
     - 
   * - admin
     - admin
     - bigint
     - 
     - 
     - True
     - 
     - FK:admin_app.models.ADMIN
   * - permission
     - permission
     - integer
     - 
     - 
     - True
     - 
     - FK:django.contrib.auth.models.Permission


Options::

 unique_together : (('admin', 'permission'),)
 default_permissions : ('add', 'change', 'delete', 'view')


admin(admin_app.models.ADMIN)
-----------------------------

::

 ADMIN(id, password, last_login, is_superuser, Email, FullName, Address, Status, Type, is_staff, is_active, Updated_At, Created_At)

.. list-table::
   :header-rows: 1

   * - Fullname
     - Name
     - Type
     - PK
     - Unique
     - Index
     - Null/Blank
     - Comment
   * - ID
     - id
     - bigint AUTO_INCREMENT
     - True
     - True
     - 
     - Blank
     - 
   * - password
     - password
     - varchar(128)
     - 
     - 
     - 
     - 
     - 
   * - last login
     - last_login
     - datetime(6)
     - 
     - 
     - 
     - Both
     - 
   * - superuser status
     - is_superuser
     - bool
     - 
     - 
     - 
     - 
     - 
   * - Email
     - Email
     - varchar(254)
     - 
     - True
     - 
     - 
     - 
   * - FullName
     - FullName
     - varchar(50)
     - 
     - 
     - 
     - 
     - 
   * - Address
     - Address
     - varchar(255)
     - 
     - 
     - 
     - 
     - 
   * - Status
     - Status
     - varchar(1)
     - 
     - 
     - 
     - 
     - A:Active, I:Inactive
   * - Type
     - Type
     - varchar(1)
     - 
     - 
     - 
     - 
     - S:Super Admin, A:Assistant Admin
   * - is staff
     - is_staff
     - bool
     - 
     - 
     - 
     - 
     - 
   * - is active
     - is_active
     - bool
     - 
     - 
     - 
     - 
     - 
   * - Updated At
     - Updated_At
     - datetime(6)
     - 
     - 
     - 
     - Blank
     - 
   * - Created At
     - Created_At
     - datetime(6)
     - 
     - 
     - 
     - Blank
     - 
   * - groups
     - groups
     - 
     - 
     - 
     - 
     - Blank
     - M2M:django.contrib.auth.models.Group (through: admin_app.models.ADMIN_groups)
   * - user permissions
     - user_permissions
     - 
     - 
     - 
     - 
     - Blank
     - M2M:django.contrib.auth.models.Permission (through: admin_app.models.ADMIN_user_permissions)


Options::

 default_permissions : ('add', 'change', 'delete', 'view')


agent(admin_app.models.AGENT)
-----------------------------

::

 AGENT(ID, Email, FullName, Address1, Address2, PhoneNumber, BirthDate, BaseCity, BaseState, Code, Status, Updated_At, Created_At)

.. list-table::
   :header-rows: 1

   * - Fullname
     - Name
     - Type
     - PK
     - Unique
     - Index
     - Null/Blank
     - Comment
   * - ID
     - ID
     - integer AUTO_INCREMENT
     - True
     - True
     - 
     - Blank
     - 
   * - Email
     - Email
     - varchar(255)
     - 
     - True
     - 
     - 
     - 
   * - FullName
     - FullName
     - varchar(50)
     - 
     - 
     - 
     - 
     - 
   * - Address1
     - Address1
     - longtext
     - 
     - 
     - 
     - 
     - 
   * - Address2
     - Address2
     - longtext
     - 
     - 
     - 
     - 
     - 
   * - PhoneNumber
     - PhoneNumber
     - varchar(50)
     - 
     - 
     - 
     - 
     - 
   * - BirthDate
     - BirthDate
     - date
     - 
     - 
     - 
     - 
     - 
   * - BaseCity
     - BaseCity
     - varchar(25)
     - 
     - 
     - 
     - 
     - 
   * - BaseState
     - BaseState
     - varchar(25)
     - 
     - 
     - 
     - 
     - 
   * - Code
     - Code
     - varchar(50)
     - 
     - True
     - 
     - 
     - 
   * - Status
     - Status
     - varchar(1)
     - 
     - 
     - 
     - 
     - A:Active, I:Inactive
   * - Updated At
     - Updated_At
     - datetime(6)
     - 
     - 
     - 
     - Blank
     - 
   * - Created At
     - Created_At
     - datetime(6)
     - 
     - 
     - 
     - Blank
     -


Options::

 default_permissions : ('add', 'change', 'delete', 'view')


setting(admin_app.models.SETTING)
---------------------------------

::

 SETTING(ID, Key, Value, Status, Updated_At, Created_At)

.. list-table::
   :header-rows: 1

   * - Fullname
     - Name
     - Type
     - PK
     - Unique
     - Index
     - Null/Blank
     - Comment
   * - ID
     - ID
     - integer AUTO_INCREMENT
     - True
     - True
     - 
     - Blank
     - 
   * - Key
     - Key
     - varchar(50)
     - 
     - 
     - 
     - 
     - 
   * - Value
     - Value
     - varchar(50)
     - 
     - 
     - 
     - 
     - 
   * - Status
     - Status
     - varchar(1)
     - 
     - 
     - 
     - 
     - A:Active, I:Inactive
   * - Updated At
     - Updated_At
     - datetime(6)
     - 
     - 
     - 
     - Blank
     - 
   * - Created At
     - Created_At
     - datetime(6)
     - 
     - 
     - 
     - Blank
     -


Options::

 default_permissions : ('add', 'change', 'delete', 'view')


category(admin_app.models.CATEGORY)
-----------------------------------

::

 CATEGORY(ID, Parent_ID, Name, Status, IconUrl, Updated_At, Created_At)

.. list-table::
   :header-rows: 1

   * - Fullname
     - Name
     - Type
     - PK
     - Unique
     - Index
     - Null/Blank
     - Comment
   * - ID
     - ID
     - integer AUTO_INCREMENT
     - True
     - True
     - 
     - Blank
     - 
   * - Parent ID
     - Parent_ID
     - integer
     - 
     - 
     - 
     - 
     - 
   * - Name
     - Name
     - varchar(50)
     - 
     - 
     - 
     - 
     - 
   * - Status
     - Status
     - varchar(1)
     - 
     - 
     - 
     - 
     - A:Active, I:Inactive
   * - IconUrl
     - IconUrl
     - varchar(100)
     - 
     - 
     - 
     - 
     - 
   * - Updated At
     - Updated_At
     - datetime(6)
     - 
     - 
     - 
     - Blank
     - 
   * - Created At
     - Created_At
     - datetime(6)
     - 
     - 
     - 
     - Blank
     -


Options::

 unique_together : (('Name', 'Parent_ID'),)
 default_permissions : ('add', 'change', 'delete', 'view')


lookupmaster(admin_app.models.LOOKUPMASTER)
-------------------------------------------

::

 LOOKUPMASTER(ID, Name, Key, Status, Updated_At, Created_At)

.. list-table::
   :header-rows: 1

   * - Fullname
     - Name
     - Type
     - PK
     - Unique
     - Index
     - Null/Blank
     - Comment
   * - ID
     - ID
     - integer AUTO_INCREMENT
     - True
     - True
     - 
     - Blank
     - 
   * - Name
     - Name
     - varchar(50)
     - 
     - 
     - 
     - 
     - 
   * - Key
     - Key
     - varchar(255)
     - 
     - True
     - 
     - 
     - 
   * - Status
     - Status
     - varchar(1)
     - 
     - 
     - 
     - 
     - A:Active, I:Inactive
   * - Updated At
     - Updated_At
     - datetime(6)
     - 
     - 
     - 
     - Blank
     - 
   * - Created At
     - Created_At
     - datetime(6)
     - 
     - 
     - 
     - Blank
     -


Options::

 default_permissions : ('add', 'change', 'delete', 'view')


lookupvalue(admin_app.models.LOOKUPVALUE)
-----------------------------------------

::

 LOOKUPVALUE(ID, MasterID, Name, Key, Updated_At, Created_At)

.. list-table::
   :header-rows: 1

   * - Fullname
     - Name
     - Type
     - PK
     - Unique
     - Index
     - Null/Blank
     - Comment
   * - ID
     - ID
     - integer AUTO_INCREMENT
     - True
     - True
     - 
     - Blank
     - 
   * - MasterID
     - MasterID
     - integer
     - 
     - 
     - True
     - 
     - FK:admin_app.models.LOOKUPMASTER
   * - Name
     - Name
     - longtext
     - 
     - 
     - 
     - 
     - 
   * - Key
     - Key
     - varchar(255)
     - 
     - 
     - 
     - 
     - 
   * - Updated At
     - Updated_At
     - datetime(6)
     - 
     - 
     - 
     - Blank
     - 
   * - Created At
     - Created_At
     - datetime(6)
     - 
     - 
     - 
     - Blank
     -


Options::

 unique_together : (('MasterID', 'Key'),)
 default_permissions : ('add', 'change', 'delete', 'view')


cms(admin_app.models.CMS)
-------------------------

::

 CMS(ID, Name, Description, Status, Updated_At, Created_At)

.. list-table::
   :header-rows: 1

   * - Fullname
     - Name
     - Type
     - PK
     - Unique
     - Index
     - Null/Blank
     - Comment
   * - ID
     - ID
     - integer AUTO_INCREMENT
     - True
     - True
     - 
     - Blank
     - 
   * - Name
     - Name
     - varchar(50)
     - 
     - True
     - 
     - 
     - 
   * - Description
     - Description
     - longtext
     - 
     - 
     - 
     - Both
     - 
   * - Status
     - Status
     - varchar(1)
     - 
     - 
     - 
     - 
     - A:Active, I:Inactive
   * - Updated At
     - Updated_At
     - datetime(6)
     - 
     - 
     - 
     - Blank
     - 
   * - Created At
     - Created_At
     - datetime(6)
     - 
     - 
     - 
     - Blank
     -


Options::

 default_permissions : ('add', 'change', 'delete', 'view')


postcodearea(admin_app.models.POSTCODEAREA)
-------------------------------------------

::

 POSTCODEAREA(ID, Name, Circle, District, Division, Region, Block, State, Country, Postcode)

.. list-table::
   :header-rows: 1

   * - Fullname
     - Name
     - Type
     - PK
     - Unique
     - Index
     - Null/Blank
     - Comment
   * - ID
     - ID
     - integer AUTO_INCREMENT
     - True
     - True
     - 
     - Blank
     - 
   * - Name
     - Name
     - varchar(100)
     - 
     - 
     - 
     - 
     - 
   * - Circle
     - Circle
     - varchar(100)
     - 
     - 
     - 
     - 
     - 
   * - District
     - District
     - varchar(100)
     - 
     - 
     - 
     - 
     - 
   * - Division
     - Division
     - varchar(100)
     - 
     - 
     - 
     - 
     - 
   * - Region
     - Region
     - varchar(100)
     - 
     - 
     - 
     - 
     - 
   * - Block
     - Block
     - varchar(100)
     - 
     - 
     - 
     - 
     - 
   * - State
     - State
     - varchar(100)
     - 
     - 
     - 
     - 
     - 
   * - Country
     - Country
     - varchar(100)
     - 
     - 
     - 
     - 
     - 
   * - Postcode
     - Postcode
     - varchar(100)
     - 
     - 
     - 
     - 
     -


Options::

 default_permissions : ('add', 'change', 'delete', 'view')


user(business_user_api.models.USER)
-----------------------------------

::

 USER(ID, CountryCode, PhoneNo, IsCustomer, IsBusiness, OtpCustomer, CustomerOtpValidUpto, OtpBusiness, BusinessOtpValidUpto, Status, Updated_At, Created_At)

.. list-table::
   :header-rows: 1

   * - Fullname
     - Name
     - Type
     - PK
     - Unique
     - Index
     - Null/Blank
     - Comment
   * - ID
     - ID
     - integer AUTO_INCREMENT
     - True
     - True
     - 
     - Blank
     - 
   * - CountryCode
     - CountryCode
     - varchar(10)
     - 
     - 
     - 
     - 
     - 
   * - PhoneNo
     - PhoneNo
     - varchar(20)
     - 
     - 
     - 
     - 
     - 
   * - IsCustomer
     - IsCustomer
     - bool
     - 
     - 
     - 
     - 
     - 
   * - IsBusiness
     - IsBusiness
     - bool
     - 
     - 
     - 
     - 
     - 
   * - OtpCustomer
     - OtpCustomer
     - varchar(6)
     - 
     - 
     - 
     - Both
     - 
   * - CustomerOtpValidUpto
     - CustomerOtpValidUpto
     - datetime(6)
     - 
     - 
     - 
     - Both
     - 
   * - OtpBusiness
     - OtpBusiness
     - varchar(6)
     - 
     - 
     - 
     - Both
     - 
   * - BusinessOtpValidUpto
     - BusinessOtpValidUpto
     - datetime(6)
     - 
     - 
     - 
     - Both
     - 
   * - Status
     - Status
     - bool
     - 
     - 
     - 
     - 
     - 
   * - Updated At
     - Updated_At
     - datetime(6)
     - 
     - 
     - 
     - Blank
     - 
   * - Created At
     - Created_At
     - datetime(6)
     - 
     - 
     - 
     - Blank
     -


Options::

 default_permissions : ('add', 'change', 'delete', 'view')


business(business_user_api.models.BUSINESS)
-------------------------------------------

::

 BUSINESS(ID, User_ID, Name, Code, Description, Address, GstNo, Contact_Person_Name, Contact_Number1, Contact_Number2, Contact_Number3, Display_NumberToCustomer, WhatsappNumber, EmailID, Category, SubCategory, Latitude, Longitude, Type, WorkingHour_Start, WorkingHour_End, Certificate1, Certificate2, Certificate3, DigitalCard_Link, FrontImageUrl, NumberOfEmployee, AgentId, BusinessType, YearOfEstablish, WebsiteLink, FacebookLink, TwitterLink, Logo, LinkedInProfile, Instagram, Status, ApproveStatus, ApprovedBy, Address1, Address2, Pincode, Area, Landmark, City, State, Step_Flag, Updated_At, Created_At)

.. list-table::
   :header-rows: 1

   * - Fullname
     - Name
     - Type
     - PK
     - Unique
     - Index
     - Null/Blank
     - Comment
   * - ID
     - ID
     - integer AUTO_INCREMENT
     - True
     - True
     - 
     - Blank
     - 
   * - User ID
     - User_ID
     - integer
     - 
     - True
     - True
     - 
     - FK:business_user_api.models.USER
   * - Name
     - Name
     - varchar(255)
     - 
     - 
     - 
     - Both
     - 
   * - Code
     - Code
     - varchar(8)
     - 
     - 
     - 
     - Both
     - 
   * - Description
     - Description
     - longtext
     - 
     - 
     - 
     - Both
     - 
   * - Address
     - Address
     - longtext
     - 
     - 
     - 
     - Both
     - 
   * - GstNo
     - GstNo
     - varchar(50)
     - 
     - 
     - 
     - Both
     - 
   * - Contact Person Name
     - Contact_Person_Name
     - varchar(255)
     - 
     - 
     - 
     - Both
     - 
   * - Contact Number1
     - Contact_Number1
     - varchar(20)
     - 
     - 
     - 
     - Both
     - 
   * - Contact Number2
     - Contact_Number2
     - varchar(20)
     - 
     - 
     - 
     - Both
     - 
   * - Contact Number3
     - Contact_Number3
     - varchar(20)
     - 
     - 
     - 
     - Both
     - 
   * - Display NumberToCustomer
     - Display_NumberToCustomer
     - varchar(1)
     - 
     - 
     - 
     - 
     - Y:Yes, N:No
   * - WhatsappNumber
     - WhatsappNumber
     - varchar(20)
     - 
     - 
     - 
     - Both
     - 
   * - EmailID
     - EmailID
     - varchar(255)
     - 
     - 
     - 
     - Both
     - 
   * - Category
     - Category
     - integer
     - 
     - 
     - True
     - Both
     - FK:admin_app.models.CATEGORY
   * - SubCategory
     - SubCategory
     - integer
     - 
     - 
     - True
     - Both
     - FK:admin_app.models.CATEGORY
   * - Latitude
     - Latitude
     - double precision
     - 
     - 
     - 
     - Both
     - 
   * - Longitude
     - Longitude
     - double precision
     - 
     - 
     - 
     - Both
     - 
   * - Type
     - Type
     - varchar(1)
     - 
     - 
     - 
     - Both
     - 1:Business, 2:Service
   * - WorkingHour Start
     - WorkingHour_Start
     - time(6)
     - 
     - 
     - 
     - Both
     - 
   * - WorkingHour End
     - WorkingHour_End
     - time(6)
     - 
     - 
     - 
     - Both
     - 
   * - Certificate1
     - Certificate1
     - varchar(255)
     - 
     - 
     - 
     - Both
     - 
   * - Certificate2
     - Certificate2
     - varchar(255)
     - 
     - 
     - 
     - Both
     - 
   * - Certificate3
     - Certificate3
     - varchar(255)
     - 
     - 
     - 
     - Both
     - 
   * - DigitalCard Link
     - DigitalCard_Link
     - varchar(255)
     - 
     - 
     - 
     - Both
     - 
   * - FrontImageUrl
     - FrontImageUrl
     - varchar(255)
     - 
     - 
     - 
     - Both
     - 
   * - NumberOfEmployee
     - NumberOfEmployee
     - integer UNSIGNED
     - 
     - 
     - 
     - Both
     - 
   * - AgentId
     - AgentId
     - integer
     - 
     - 
     - True
     - Both
     - FK:admin_app.models.AGENT
   * - BusinessType
     - BusinessType
     - integer
     - 
     - 
     - True
     - Both
     - FK:admin_app.models.LOOKUPVALUE
   * - YearOfEstablish
     - YearOfEstablish
     - datetime(6)
     - 
     - 
     - 
     - Both
     - 
   * - WebsiteLink
     - WebsiteLink
     - varchar(255)
     - 
     - 
     - 
     - Both
     - 
   * - FacebookLink
     - FacebookLink
     - varchar(255)
     - 
     - 
     - 
     - Both
     - 
   * - TwitterLink
     - TwitterLink
     - varchar(255)
     - 
     - 
     - 
     - Both
     - 
   * - Logo
     - Logo
     - varchar(255)
     - 
     - 
     - 
     - Both
     - 
   * - LinkedInProfile
     - LinkedInProfile
     - varchar(255)
     - 
     - 
     - 
     - Both
     - 
   * - Instagram
     - Instagram
     - varchar(255)
     - 
     - 
     - 
     - Both
     - 
   * - Status
     - Status
     - bool
     - 
     - 
     - 
     - 
     - 
   * - ApproveStatus
     - ApproveStatus
     - varchar(1)
     - 
     - 
     - 
     - Both
     - Y:Yes, N:No
   * - ApprovedBy
     - ApprovedBy
     - bigint
     - 
     - 
     - True
     - Both
     - FK:admin_app.models.ADMIN
   * - Address1
     - Address1
     - varchar(255)
     - 
     - 
     - 
     - Both
     - 
   * - Address2
     - Address2
     - varchar(255)
     - 
     - 
     - 
     - Both
     - 
   * - Pincode
     - Pincode
     - integer UNSIGNED
     - 
     - 
     - 
     - Both
     - 
   * - Area
     - Area
     - varchar(255)
     - 
     - 
     - 
     - Both
     - 
   * - Landmark
     - Landmark
     - varchar(255)
     - 
     - 
     - 
     - Both
     - 
   * - City
     - City
     - varchar(255)
     - 
     - 
     - 
     - Both
     - 
   * - State
     - State
     - varchar(255)
     - 
     - 
     - 
     - Both
     - 
   * - Step Flag
     - Step_Flag
     - integer UNSIGNED
     - 
     - 
     - 
     - 
     - 
   * - Updated At
     - Updated_At
     - datetime(6)
     - 
     - 
     - 
     - Blank
     - 
   * - Created At
     - Created_At
     - datetime(6)
     - 
     - 
     - 
     - Blank
     -


Options::

 default_permissions : ('add', 'change', 'delete', 'view')


customer(business_user_api.models.CUSTOMER)
-------------------------------------------

::

 CUSTOMER(ID, User_ID, Name, Gender, Contact_Number, Display_NuTobusiness, Email_ID, Address, Post_Code, Landmark, City, State, Status, Updated_At, Created_At)

.. list-table::
   :header-rows: 1

   * - Fullname
     - Name
     - Type
     - PK
     - Unique
     - Index
     - Null/Blank
     - Comment
   * - ID
     - ID
     - integer AUTO_INCREMENT
     - True
     - True
     - 
     - Blank
     - 
   * - User ID
     - User_ID
     - integer
     - 
     - True
     - True
     - 
     - FK:business_user_api.models.USER
   * - Name
     - Name
     - varchar(256)
     - 
     - 
     - 
     - 
     - 
   * - Gender
     - Gender
     - integer
     - 
     - 
     - True
     - 
     - FK:admin_app.models.LOOKUPVALUE
   * - Contact Number
     - Contact_Number
     - varchar(255)
     - 
     - 
     - 
     - Both
     - 
   * - Display NuTobusiness
     - Display_NuTobusiness
     - varchar(1)
     - 
     - 
     - 
     - 
     - Y:Yes, N:No
   * - Email ID
     - Email_ID
     - varchar(255)
     - 
     - 
     - 
     - 
     - 
   * - Address
     - Address
     - varchar(255)
     - 
     - 
     - 
     - 
     - 
   * - Post Code
     - Post_Code
     - varchar(255)
     - 
     - 
     - 
     - 
     - 
   * - Landmark
     - Landmark
     - varchar(255)
     - 
     - 
     - 
     - 
     - 
   * - City
     - City
     - varchar(255)
     - 
     - 
     - 
     - 
     - 
   * - State
     - State
     - varchar(255)
     - 
     - 
     - 
     - 
     - 
   * - Status
     - Status
     - bool
     - 
     - 
     - 
     - 
     - 
   * - Updated At
     - Updated_At
     - datetime(6)
     - 
     - 
     - 
     - Blank
     - 
   * - Created At
     - Created_At
     - datetime(6)
     - 
     - 
     - 
     - Blank
     -


Options::

 default_permissions : ('add', 'change', 'delete', 'view')


suppor t_ticket(business_user_api.models.SUPPORT_TICKET)
--------------------------------------------------------

::

 SUPPORT_TICKET(ID, Business_id, Title, Description, Status, Updated_At, Created_At)

.. list-table::
   :header-rows: 1

   * - Fullname
     - Name
     - Type
     - PK
     - Unique
     - Index
     - Null/Blank
     - Comment
   * - ID
     - ID
     - integer AUTO_INCREMENT
     - True
     - True
     - 
     - Blank
     - 
   * - Business id
     - Business_id
     - integer
     - 
     - 
     - True
     - 
     - FK:business_user_api.models.BUSINESS
   * - Title
     - Title
     - varchar(50)
     - 
     - 
     - 
     - 
     - 
   * - Description
     - Description
     - longtext
     - 
     - 
     - 
     - 
     - 
   * - Status
     - Status
     - varchar(1)
     - 
     - 
     - 
     - 
     - O:Open, P:In Process, A:Close, D:Delete
   * - Updated At
     - Updated_At
     - datetime(6)
     - 
     - 
     - 
     - Blank
     - 
   * - Created At
     - Created_At
     - datetime(6)
     - 
     - 
     - 
     - Blank
     -


Options::

 default_permissions : ('add', 'change', 'delete', 'view')


suppor t_ticke t_reply(business_user_api.models.SUPPORT_TICKET_REPLY)
---------------------------------------------------------------------

::

 SUPPORT_TICKET_REPLY(ID, Ticket_ID, Description, Replyby, Related_ID, Created_At, Updated_At)

.. list-table::
   :header-rows: 1

   * - Fullname
     - Name
     - Type
     - PK
     - Unique
     - Index
     - Null/Blank
     - Comment
   * - ID
     - ID
     - integer AUTO_INCREMENT
     - True
     - True
     - 
     - Blank
     - 
   * - Ticket ID
     - Ticket_ID
     - integer
     - 
     - 
     - True
     - 
     - FK:business_user_api.models.SUPPORT_TICKET
   * - Description
     - Description
     - longtext
     - 
     - 
     - 
     - 
     - 
   * - Replyby
     - Replyby
     - varchar(1)
     - 
     - 
     - 
     - 
     - A:Admin, B:Bunsiness
   * - Related ID
     - Related_ID
     - integer UNSIGNED
     - 
     - 
     - 
     - 
     - 
   * - Created At
     - Created_At
     - datetime(6)
     - 
     - 
     - 
     - Blank
     - 
   * - Updated At
     - Updated_At
     - datetime(6)
     - 
     - 
     - 
     - Blank
     -


Options::

 default_permissions : ('add', 'change', 'delete', 'view')


ap p_version(business_user_api.models.APP_VERSION)
--------------------------------------------------

::

 APP_VERSION(ID, App_Type, Version, Status, Updated_At, Created_At)

.. list-table::
   :header-rows: 1

   * - Fullname
     - Name
     - Type
     - PK
     - Unique
     - Index
     - Null/Blank
     - Comment
   * - ID
     - ID
     - integer AUTO_INCREMENT
     - True
     - True
     - 
     - Blank
     - 
   * - App Type
     - App_Type
     - varchar(1)
     - 
     - 
     - 
     - 
     - 0:ANDROID, 1:IOS
   * - Version
     - Version
     - double precision
     - 
     - 
     - 
     - 
     - 
   * - Status
     - Status
     - bool
     - 
     - 
     - 
     - 
     - 
   * - Updated At
     - Updated_At
     - datetime(6)
     - 
     - 
     - 
     - Blank
     - 
   * - Created At
     - Created_At
     - datetime(6)
     - 
     - 
     - 
     - Blank
     -


Options::

 default_permissions : ('add', 'change', 'delete', 'view')


offer(business_user_api.models.OFFER)
-------------------------------------

::

 OFFER(ID, Business_ID, Title, Description, ImageUrl, StartDate, EndDate, Status, Updated_At, Created_At)

.. list-table::
   :header-rows: 1

   * - Fullname
     - Name
     - Type
     - PK
     - Unique
     - Index
     - Null/Blank
     - Comment
   * - ID
     - ID
     - integer AUTO_INCREMENT
     - True
     - True
     - 
     - Blank
     - 
   * - Business ID
     - Business_ID
     - integer
     - 
     - 
     - True
     - 
     - FK:business_user_api.models.BUSINESS
   * - Title
     - Title
     - varchar(256)
     - 
     - 
     - 
     - 
     - 
   * - Description
     - Description
     - longtext
     - 
     - 
     - 
     - 
     - 
   * - ImageUrl
     - ImageUrl
     - varchar(100)
     - 
     - 
     - 
     - 
     - 
   * - StartDate
     - StartDate
     - datetime(6)
     - 
     - 
     - 
     - 
     - 
   * - EndDate
     - EndDate
     - datetime(6)
     - 
     - 
     - 
     - 
     - 
   * - Status
     - Status
     - bool
     - 
     - 
     - 
     - 
     - 
   * - Updated At
     - Updated_At
     - datetime(6)
     - 
     - 
     - 
     - Blank
     - 
   * - Created At
     - Created_At
     - datetime(6)
     - 
     - 
     - 
     - Blank
     -


Options::

 unique_together : (('Business_ID', 'Title'),)
 default_permissions : ('add', 'change', 'delete', 'view')


log entry(django.contrib.admin.models.LogEntry)
-----------------------------------------------

::

 LogEntry(id, action_time, user, content_type, object_id, object_repr, action_flag, change_message)

.. list-table::
   :header-rows: 1

   * - Fullname
     - Name
     - Type
     - PK
     - Unique
     - Index
     - Null/Blank
     - Comment
   * - ID
     - id
     - integer AUTO_INCREMENT
     - True
     - True
     - 
     - Blank
     - 
   * - action time
     - action_time
     - datetime(6)
     - 
     - 
     - 
     - 
     - 
   * - user
     - user
     - bigint
     - 
     - 
     - True
     - 
     - FK:admin_app.models.ADMIN
   * - content type
     - content_type
     - integer
     - 
     - 
     - True
     - Both
     - FK:django.contrib.contenttypes.models.ContentType
   * - object id
     - object_id
     - longtext
     - 
     - 
     - 
     - Both
     - 
   * - object repr
     - object_repr
     - varchar(200)
     - 
     - 
     - 
     - 
     - 
   * - action flag
     - action_flag
     - smallint UNSIGNED
     - 
     - 
     - 
     - 
     - 1:Addition, 2:Change, 3:Deletion
   * - change message
     - change_message
     - longtext
     - 
     - 
     - 
     - Blank
     -


Options::

 ordering : ['-action_time']
 default_permissions : ('add', 'change', 'delete', 'view')


permission(django.contrib.auth.models.Permission)
-------------------------------------------------

::

 
    The permissions system provides a way to assign permissions to specific
    users and groups of users.

    The permission system is used by the Django admin site, but may also be
    useful in your own code. The Django admin site uses permissions as follows:

        - The "add" permission limits the user's ability to view the "add" form
          and add an object.
        - The "change" permission limits a user's ability to view the change
          list, view the "change" form and change an object.
        - The "delete" permission limits the ability to delete an object.
        - The "view" permission limits the ability to view an object.

    Permissions are set globally per type of object, not per specific object
    instance. It is possible to say "Mary may change news stories," but it's
    not currently possible to say "Mary may change news stories, but only the
    ones she created herself" or "Mary may only change news stories that have a
    certain status or publication date."

    The permissions listed above are automatically created for each model.
    

.. list-table::
   :header-rows: 1

   * - Fullname
     - Name
     - Type
     - PK
     - Unique
     - Index
     - Null/Blank
     - Comment
   * - ID
     - id
     - integer AUTO_INCREMENT
     - True
     - True
     - 
     - Blank
     - 
   * - name
     - name
     - varchar(255)
     - 
     - 
     - 
     - 
     - 
   * - content type
     - content_type
     - integer
     - 
     - 
     - True
     - 
     - FK:django.contrib.contenttypes.models.ContentType
   * - codename
     - codename
     - varchar(100)
     - 
     - 
     - 
     - 
     -


Options::

 unique_together : (('content_type', 'codename'),)
 ordering : ['content_type__app_label', 'content_type__model', 'codename']
 default_permissions : ('add', 'change', 'delete', 'view')


group-permission relationship(django.contrib.auth.models.Group_permissions)
---------------------------------------------------------------------------

::

 Group_permissions(id, group, permission)

.. list-table::
   :header-rows: 1

   * - Fullname
     - Name
     - Type
     - PK
     - Unique
     - Index
     - Null/Blank
     - Comment
   * - ID
     - id
     - integer AUTO_INCREMENT
     - True
     - True
     - 
     - Blank
     - 
   * - group
     - group
     - integer
     - 
     - 
     - True
     - 
     - FK:django.contrib.auth.models.Group
   * - permission
     - permission
     - integer
     - 
     - 
     - True
     - 
     - FK:django.contrib.auth.models.Permission


Options::

 unique_together : (('group', 'permission'),)
 default_permissions : ('add', 'change', 'delete', 'view')


group(django.contrib.auth.models.Group)
---------------------------------------

::

 
    Groups are a generic way of categorizing users to apply permissions, or
    some other label, to those users. A user can belong to any number of
    groups.

    A user in a group automatically has all the permissions granted to that
    group. For example, if the group 'Site editors' has the permission
    can_edit_home_page, any user in that group will have that permission.

    Beyond permissions, groups are a convenient way to categorize users to
    apply some label, or extended functionality, to them. For example, you
    could create a group 'Special users', and you could write code that would
    do special things to those users -- such as giving them access to a
    members-only portion of your site, or sending them members-only email
    messages.
    

.. list-table::
   :header-rows: 1

   * - Fullname
     - Name
     - Type
     - PK
     - Unique
     - Index
     - Null/Blank
     - Comment
   * - ID
     - id
     - integer AUTO_INCREMENT
     - True
     - True
     - 
     - Blank
     - 
   * - name
     - name
     - varchar(150)
     - 
     - True
     - 
     - 
     - 
   * - permissions
     - permissions
     - 
     - 
     - 
     - 
     - Blank
     - M2M:django.contrib.auth.models.Permission (through: django.contrib.auth.models.Group_permissions)


Options::

 default_permissions : ('add', 'change', 'delete', 'view')


content type(django.contrib.contenttypes.models.ContentType)
------------------------------------------------------------

::

 ContentType(id, app_label, model)

.. list-table::
   :header-rows: 1

   * - Fullname
     - Name
     - Type
     - PK
     - Unique
     - Index
     - Null/Blank
     - Comment
   * - ID
     - id
     - integer AUTO_INCREMENT
     - True
     - True
     - 
     - Blank
     - 
   * - app label
     - app_label
     - varchar(100)
     - 
     - 
     - 
     - 
     - 
   * - python model class name
     - model
     - varchar(100)
     - 
     - 
     - 
     - 
     -


Options::

 unique_together : (('app_label', 'model'),)
 default_permissions : ('add', 'change', 'delete', 'view')


session(django.contrib.sessions.models.Session)
-----------------------------------------------

::

 
    Django provides full support for anonymous sessions. The session
    framework lets you store and retrieve arbitrary data on a
    per-site-visitor basis. It stores data on the server side and
    abstracts the sending and receiving of cookies. Cookies contain a
    session ID -- not the data itself.

    The Django sessions framework is entirely cookie-based. It does
    not fall back to putting session IDs in URLs. This is an intentional
    design decision. Not only does that behavior make URLs ugly, it makes
    your site vulnerable to session-ID theft via the "Referer" header.

    For complete documentation on using Sessions in your code, consult
    the sessions documentation that is shipped with Django (also available
    on the Django web site).
    

.. list-table::
   :header-rows: 1

   * - Fullname
     - Name
     - Type
     - PK
     - Unique
     - Index
     - Null/Blank
     - Comment
   * - session key
     - session_key
     - varchar(40)
     - True
     - True
     - 
     - 
     - 
   * - session data
     - session_data
     - longtext
     - 
     - 
     - 
     - 
     - 
   * - expire date
     - expire_date
     - datetime(6)
     - 
     - 
     - True
     - 
     -


Options::

 default_permissions : ('add', 'change', 'delete', 'view')



