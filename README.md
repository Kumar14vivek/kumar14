# kumar14

select VC_COMP_CODE,
    VC_VOUCHER_NO,
    DT_VOUCHER_DATE,
    DEBIT,
    CREDIT, debit-credit diff
     from mismatch
     group by VC_COMP_CODE,
    VC_VOUCHER_NO,
    DT_VOUCHER_DATE,
    DEBIT,
    CREDIT
 having round(debit-credit,0)<>0
