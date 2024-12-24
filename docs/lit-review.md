<!--- file: docs/howto/embedding_pdf.md --->
{% with pdf_file = "artifacts/file.pdf" %}

{% set solid_filepdf = '<i class="fas fa-file-pdf"></i>' %}
{% set empty_filepdf = '<i class="far fa-file-pdf"></i>' %}


<object data="{{ pdfs/Alcraft_LitReview_2022.pdf }}" type="application/pdf">
    <embed src="{{ pdfs/Alcraft_LitReview_2022.pdf }}" type="application/pdf" />
</object>
