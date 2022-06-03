<template>
  <v-card class="bodyCardContainer">
    <v-layout row wrap>
      <v-flex xs12 md4 class="bodyCardAvatarQual">
        <br />
        <v-avatar size="130">
          <v-img src="../assets/item_logo/aws_logo.png" />
        </v-avatar>
        <br />
      </v-flex>
      <v-flex xs12 md8>
        <span class="bodyCardDateText">{{issuedDate}} - {{expiredDate}}</span>
        <br />
        <span class="bodyCardTitle">{{certName}}</span>
        <br />
        <p class="bodyCardText" v-for="detail in certDetail" :key="detail">{{detail}}</p>
        <ul>
          <li class="bodyCardTextList" v-for="content in contentList" :key="content">{{content}}</li>
        </ul>
        <br/>
      </v-flex>
    </v-layout>
  </v-card>
</template>

<script>
export default {
  name: "AwsSolutionAsso",
  data: () => ({
    iconUrl: "aws_logo",
    certName: "AWS Certified Solutions Architect - Associate",
    issuedOrg: "AWS Training and Certification",
    issuedDate: "Jan 2022",
    expiredDate: "Jan 2025",
    certDetail: [
      "Issued by AWS Training and Certification",
      "Ability to build secure and robust solutions using architectural design principles based on customer requirements and to strategically design well-architected distributed systems that are scalable, resilient, efficient, and fault-tolerant",
    ],
    contentList: [
      "Application Integration (Amazon SQS, Amazon SNS)",
      "Compute (Amazon EC2, AWS Lambda)",
      "Database (Amazon DynamoDB, Amazon ElastiCache, Amazon Redshift)",
      "Management and Governance (AWS CloudTrail, Amazon CloudWatch)",
      "Networking and Content Delivery (Amazon API Gateway)",
      "Security, Identity, and Compliance (AWS IAM)",
      "Storage (Amazon EFS, Amazon S3)",
    ]
  }),
};
</script>
