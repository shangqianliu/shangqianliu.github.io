---
layout: post
title: 银行业务核心系统（初识）
description: 一些不错的知识点，持续更新。
category: blog
---

定义：
核心银行系统是银行实现客户关系管理、集成交易处理、产品与服务
创新、风险的管控、资本配置等多个应用组成系统。是银行信息系统的
基础与核心，是银行的心脏，也称Core Banking 。主要完成存款、贷款业务
操作都是在银行核心业务中完成的。
它也可以是一个系统群。存款贷款，支付结算都属于核心业务范畴。但是其中贷款的账务处理
和贷款的授信、审批以及贷后管理就不放在一个系统里。账务处理力求稳定和高效。
而贷款流程管理力求灵活多变，不同的功能放到不同的系统中处理。
08年之后银行大前置、精于核心（去除大部分管理功能）的概念。
https://blog.csdn.net/ss123465/article/details/7979464
----完成人民银行或中国金融市场规定的支付业务、结算业务、存款业务、贷款业务中的账务处理
和会计处理-----单纯的交易处理系统。
-------核心系统缩减功能为了提升系统运行的效率和架构稳定。（虽然效率和架构有效提升但是操作数据没有保留，没有完善的风险控制机制）
多管理业务有一站式服务，但是功能结构复杂，修改要求高。


逻辑结构：业务管理层和业务处理层，前者为后者提供服务。费用管理，假期管理，利率，汇率，机构，凭证，用户管理模块。
功能模块结构：公共业务员，客户信息，存款，贷款。资金业务，国际结算，总账，卡系统等等。
客户信息模块（CI）:主要记录单位、个人、机构的基本信息、联系方式、签约信息、及与账户的
关联关系，（我的理解相当于数据库主表）担任着与各模块或外围系统提供统一的视图。主表中的
主键（客户号）-------一个客户号对应一个客户，而一个客户可以在本行开立多个账户，活期、定期
贷款。开户分为很多种：单位，个人，机构。





公共业务模块是核心业务系统的公共模块，主要是为了其他模块提供服务与支持的模块，包括的交易有：当日冲正、隔日冲正、工作量复核、交易历史查询、参数维护等”
其中用户管理，也是柜台管理，登录前端系统的ID.事实上使用系统的用户未必都是柜员，还有很多
功能，新增柜员、删除柜员、修改柜员密码、修改柜员资料（级别/姓名/电话）、柜员休假/销假/离职
、柜员业务权限设置、柜员日结单打印、等等。按照操作权限可以分为现金柜员、凭证柜员、账务柜员、授权柜员和经办人员等。系统用户分为真实用户和虚拟用户，真实用户是真实姓名，而虚拟用户
是虚设的，比如跑批柜员，在跑批过程中可以登录系统，或系统在跑批过程中形成的账户以跑批柜员的ID记账。
机构模块：用于维护系统内各级经营管理的机构，比如上级清算行、上级行清算账户、人行清算账号
支付系统行号、同城交换号、交换场次、地址、联系电话。
机构层级可以分为总行、分行和支行三大类，按功能又可以分为营业机构（存蓄所、分理所、营业部）和内部机构（本级直营机构、财务机构、专业处理中心）。还有一些特殊功能（新设、分设、撤并）
-----------------------------------------
存款模块可以分为个人和对公两大类。
个人常见功能：本外币开户、现金存入/支取、活期转账、定期开户、销户、密码/凭证挂失解挂
和密码维护、睡眠户/不动户办理、开立存款证明或支票、换折或补登折、定期提前支取、计息调整
、单位交易有活期开销户、存入/支取和转账、定期部提和结清、通知存款预约、签约单位协定存款
印鉴挂失/解挂、账户冻结/解冻。
不同银行所支持的功能有些差别。
贷款模块主要负责贷款的会计处理，相关的交易有贷款开户、贷款正常还本利息、逾期贷款还本利息
贷款展期、贷款销户、不良贷款核销、贷款信息修改、票据贴现（或转贴现、再贴现）、回购方式贴现赎回、出口押汇等等。支付结算主要处理银行与客户之间因结算引起的转账处理，也包括机构内的转账。比如银行汇票处理（包括签发、代理签发、资金转移、兑付、打印、余款退回、入账）商业汇票处理（签发、承兑、结算、提示付款）、大额汇出/汇入汇款、小额汇出/汇入汇款、支付报文打印
提出贷方、提入借方、本票兑付、托收入账、托收承付、托收入账、支付系统对账、支付系统差错处理、支付系统日期管理等。





