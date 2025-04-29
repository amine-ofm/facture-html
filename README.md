<!DOCTYPE html>
<html>
  <head>
    <meta charset="UTF-8">
    <title>Facture</title>
    <style>
      body { font-family: Arial, sans-serif; margin: 40px; }
      h1 { text-align: center; }
      table { width: 100%; border-collapse: collapse; margin-top: 30px; }
      td, th { padding: 10px; border: 1px solid #ddd; text-align: left; }
      .footer { margin-top: 40px; font-size: 0.9em; }
    </style>
  </head>
  <body>
    <h1>FACTURE</h1>

    <p><strong>Client :</strong> {{ $json.nomClient }}</p>
    <p><strong>Adresse :</strong> {{ $json.adresse }}</p>
    <p><strong>Matricule fiscale :</strong> {{ $('Edit Fields').item.json['Matricule Fiscale'] }}</p>
    <p><strong>Email :</strong> {{ $('Edit Fields').item.json['Adresse Email'] }}</p>

    <table>
      <tr>
        <th>Description</th>
        <th>Montant (DT)</th>
      </tr>
      <tr>
        <td>Montant HT</td>
        <td>{{ $json.montantHT }}</td>
      </tr>
      <tr>
        <td>TVA (19%)</td>
        <td>{{ $json.tva }}</td>
      </tr>
      <tr>
        <td>Retenue à la source (3%)</td>
        <td>-{{ $json.retenueSource }}</td>
      </tr>
      <tr>
        <td>Timbre fiscal</td>
        <td>{{ $json.timbreFiscal }}</td>
      </tr>
      <tr>
        <th>Total TTC</th>
        <th>{{ $json.montantTTC }}</th>
      </tr>
    </table>

    <div class="footer">
      <p>Merci pour votre confiance.</p>
    </div>
  </body>
</html>
