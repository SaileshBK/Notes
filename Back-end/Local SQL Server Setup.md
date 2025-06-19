## Ways to setup local SQL db server 

1) To create a local DB instance:

    `sqllocaldb create "TestSQLInstance"`

    This will create a LocalDB instance "TestSQLInstance" created with version x.x.x.x

2) Now you have an instance, we can check the status of the instance:

    `sqllocaldb info "TestSQLInstance"`

    here the status of the instance will be displayed with stopped state. We can start the instance by
    using:

    `sqllocaldb start "TestSQLInstance"`

3) Now you can just connect with this instance using SSMS (SQL Server Management Studio). Make 
    sure the Server name is '(localdb)\TestSQLInstance' and you have Windows Authentication mode set.
