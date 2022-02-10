### Developer Task 1 

* Following is the different bugs that were identified in this exercise.

### Bug : Non static variabe LOGGER cannot be referenced from a static context
***
[INFO] Finished at: 2022-02-10T12:12:08+03:00
[INFO] ------------------------------------------------------------------------
[ERROR] Failed to execute goal org.apache.maven.plugins:maven-compiler-plugin:3.1:compile (default-compile) on project econet-utils: Compilation failure: Compilation failure:
[ERROR] /C:/Users/hp/Desktop/Workspace/project_template/econet-utils/src/main/java/com/econetwireless/utils/formatters/MobileNumberUtils.java:[36,13] non-static variable LOGGER cannot be referenced from a static context

***


### Bug : Class @Preinsert  does not exist 
*** Failed to execute goal org.apache.maven.plugins:maven-compiler-plugin:3.1:compile (default-compile) on project electronic-payments-domain: Compilation failure
[ERROR] /C:/Users/hp/Desktop/Workspace/project_template/electronic-payments-domain/src/main/java/com/econetwireless/epay/domain/SubscriberRequest.java:[42,6] cannot find symbol
[ERROR]   symbol:   class PreInsert
[ERROR]   location: class com.econetwireless.epay.domain.SubscriberRequest
***


### Bug: Incorrect use of super and this key words in the constructor
***
Failed to execute goal org.apache.maven.plugins:maven-compiler-plugin:3.1:compile (default-compile) on project electronic-payments-business: Compilation failure: Compilation failure:
[ERROR] /C:/Users/hp/Desktop/Workspace/project_template/electronic-payments-business/src/main/java/com/econetwireless/epay/business/services/impl/PartnerCodeValidatorImpl.java:[16,19] '.' expected
[ERROR] /C:/Users/hp/Desktop/Workspace/project_template/electronic-payments-business/src/main/java/com/econetwireless/epay/business/services/impl/PartnerCodeValidatorImpl.java:[16,20] ')' expected
[ERROR] /C:/Users/hp/Desktop/Workspace/project_template/electronic-payments-business/src/main/java/com/econetwireless/epay/business/services/impl/PartnerCodeValidatorImpl.java:[16,21] ';' expected
[ERROR] /C:/Users/hp/Desktop/Workspace/project_template/electronic-payments-business/src/main/java/com/econetwireless/epay/business/services/impl/PartnerCodeValidatorImpl.java:[17,13] illegal start of expression
***

### Bug: Methods update and exist cannot be found variabe of type subscriberRequestDao

***
/C:/Users/hp/Desktop/Workspace/project_template/electronic-payments-business/src/main/java/com/econetwireless/epay/business/services/impl/EnquiriesServiceImpl.java:[36,80] cannot find symbol
[ERROR]   symbol:   method persist(com.econetwireless.epay.domain.SubscriberRequest)
[ERROR]   location: variable subscriberRequestDao of type com.econetwireless.epay.dao.subscriberrequest.api.SubscriberRequestDao
[ERROR] /C:/Users/hp/Desktop/Workspace/project_template/electronic-payments-business/src/main/java/com/econetwireless/epay/business/services/impl/EnquiriesServiceImpl.java:[39,29] cannot find symbol
[ERROR]   symbol:   method update(com.econetwireless.epay.domain.SubscriberRequest)
[ERROR]   location: variable subscriberRequestDao of type com.econetwireless.epay.dao.subscriberrequest.api.SubscriberRequestDao
[ERROR] /C:/Users/hp/Desktop/Workspace/project_template/electronic-payments-business/src/main/java/com/econetwireless/epay/business/services/impl/CreditsServiceImpl.java:[38,80] cannot find symbol
[ERROR]   symbol:   method persist(com.econetwireless.epay.domain.SubscriberRequest)
[ERROR]   location: variable subscriberRequestDao of type com.econetwireless.epay.dao.subscriberrequest.api.SubscriberRequestDao
[ERROR] /C:/Users/hp/Desktop/Workspace/project_template/electronic-payments-business/src/main/java/com/econetwireless/epay/business/services/impl/CreditsServiceImpl.java:[41,29] cannot find symbol
[ERROR]   symbol:   method update(com.econetwireless.epay.domain.SubscriberRequest)
[ERROR]   location: variable subscriberRequestDao of type com.econetwireless.epay.dao.subscriberrequest.api.SubscriberRequestDao
***

### Bug: Incorrect table name used in SQL Query 
***
ERROR org.hibernate.internal.SessionFactoryImpl - HHH000177: Error in named query: SubscriberRequest.findByPartnerCode
org.hibernate.hql.internal.ast.QuerySyntaxException: Request is not mapped [select r from Request r where r.partnerCode = :partnerCode order by r.dateCreated desc ]
***

### Test Fail:  Request processing failed; nested exception is java.lang.NullPointerException

***
Tests in error:
shouldReturnStatusOkIfRequestsAreMoreThanOne(com.econetwireless.epay.api.rest.resources.EpayResourcesIT): Request processing failed; nested exception is java.lang.NullPointerException
airtimeTopupShouldReturnResponseCodeSUCCESSIfAllOtherSystemsAreUp(com.econetwireless.epay.api.rest.resources.EpayResourcesIT): Request processing failed; nested exception is java.lang.NullPointerException
airtimeBalanceEnquiryShouldReturnResponseCodeSUCCESSIfAllOtherSystemsAreUp(com.econetwireless.epay.api.rest.resources.EpayResourcesIT): Request processing failed; nested exception is java.lang.NullPointerException
***

#### Additional Notes 

1. Resolved dependency conflicts by downgrading to JDK 8 from 17.