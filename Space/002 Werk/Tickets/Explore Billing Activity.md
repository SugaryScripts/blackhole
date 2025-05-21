File Location :
# FE
src\app\accmnt\billing\general\billing-activity\billing-activity-paging\billing-activity-paging.component.ts
src\assets\ucpaging\accmnt\billing\general\search-billing-activity.json
src\app\accmnt\billing\general\billing-activity\billing-activity-detail\billing-activity-detail.component.ts

# BE
Submit print billing, download invoice, submit input billing activity
\r3_taf_lms_core_be_docs\AdIns.LMS.BusinessService\TransactionService\BillTrxActivityHistOplTrService.cs

Generate report R3
\r3_taf_fou_core_be_docs\_REPORT\AdIns.ReportGenerator.BusinessService\ReportGeneratorService.cs
	\r3_taf_lms_report\AdIns.Report.LMS\AdIns_GenerateLMSInvoice.rdlc


Action:
Activity navigasi ke BILLING_ACTIVITY_DETAIL untuk di submit

QueryPaging: searchBillingActivity
Table dari BILL_TRX_OPL dan join dengan BILL_GRP_H_OPL
Syarat BILL_TRX_OPL harus aktif

Validation print
- tipe bill harus rent
- VAT invoice Optional?

**Print**
API /BillActivity/SubmitPrintBilling
- empty
API /BillActivity/DownloadInvoice
- Untuk mendapatkan response VAT Invoice, jika tidak ada response muncul error VAT Invoice PDF File not found
API /Report/GenerateReportR3
- Untuk generate report dari data yang telah di tambahkan pakai button add to temp, di mana file PDF otomatis terdownload BILA return response

**Activity Submit**
Daftar data billnya didapat dari billActivityService lalu ditransfer ke variable ListBillTrxOplId dan ListItem
Activity Date secara default adalah business date => validasi frontend maximum business date
API /BillActivity/SubmitInputBillingActivity
- submit activity


# BE
API /BillActivity/SubmitPrintBilling => LMS.Core
- Membuat BillTrxActivityHistOpl baru dan update BillTrxOpl
- update apabila isUpdateBillTrxOpl maka get data lalu update datanya berdasarkan parameter yang diterima
API /BillActivity/DownloadInvoice => LMS.Core
- Mencari dulu BillTrxOpl by bill id, lalu cari UploadMonitoringVatD by bill no
- Return pdf yang bernama invoice.pdf jika ditemukan
API /Report/GenerateReportR3 => FOU.X
- Ambil dari table RptList dari FOU untuk dibuatkan reportnya -> nanti dapat template code beserta pathnya
- Template reportnya dari path yang sudah didapet AdIns_GenerateLMSInvoice.rdlc


API /BillActivity/SubmitInputBillingActivity => LMS.Core
- Buat BillTrxActivityHistOpl baru