```
--------------------------------------------------------------------------------
---��ѯ���е���������--Ψһ����
select COUNT(*)  INTO INDEXNUM
  from user_indexes
 where table_name = '����'
   AND INDEX_NAME = '��������';
  AND UNIQUENESS='UNIQUE/NOUNIQUE';

---ɾ��һ������   
drop index ��������;
--ɾ��Ψһ����
alter table ���� drop constraint ��������
 
 
----------------------------------------------------------------------------------
---��ѯ������
SELECT count(*) INTO COLUMNNUM FROM USER_TAB_COLUMNS where TABLE_NAME='����' AND COLUMN_NAME='����';
--����һ�У�

   alter table ���� add ���� varchar2(10);

--�޸�һ�У�

   alter table ���� modify �б� varchar2(20);

--ɾ��һ�У�

alter table ���� drop column ����;

-----------------------------------------------------------------------------------------------------
---��ѯ���Լ��
select count(*) INTO constraintnum from user_cons_columns cl where cl.constraint_name = 'Լ������' AND TABLE_NAME='����';

--���һ������Լ��  
alter table ���� add constraint Լ���� primary key (����);  

alter table Լ�����ڵı��� drop constraint Լ����;

--����Լ��
alter table table_name rename constraint �ɵ�Լ������ to �µ�Լ������;

--Լ����Ч/��Ч
alter table table_name enable/disable constraint Լ������;

----------------------------------------------------------------------------------
---��ѯ�ñ��Ƿ����
select  count(*) INTO TABLENUM from   user_tables WHERE TABLE_NAME='����';
--ɾ����
drop table ����;



----ģ��������-----
DECLARE 
 INDEXNUM NUMBER;
 begin
 INDEXNUM:=0;
 
 select COUNT(*)  INTO INDEXNUM
  from user_indexes
 where table_name = 'UEM_EMP'
   AND INDEX_NAME = 'UI_UEM_EMP'
   AND UNIQUENESS='UNIQUE';
   
 if INDEXNUM>0 THEN
 Execute immediate 'alter table ���� drop constraint ��������';
 
  END IF;
  
 if INDEXNUM=0 then
  Execute immediate 'ALTER table ���� add constraint UI_UEM_EMP unique (����)
  using index 
  tablespace KDBASE_DATA
  pctfree 10
  initrans 2
  maxtrans 255
  storage
  (
    initial 64K
    next 1M
    minextents 1
    maxextents unlimited
  )';
  end if;
  end;
  
```  