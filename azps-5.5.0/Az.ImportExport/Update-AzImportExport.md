---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/update-azimportexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Update-AzImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Update-AzImportExport.md
ms.openlocfilehash: d6ed55cef91dc93f0ce9101adf94d9dc6931d07c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100237678"
---
# Update-AzImportExport

## SYNOPSIS
Uppdaterar specifika egenskaper för ett jobb.
Du kan anropa den här åtgärden om du vill meddela import-/exporttjänsten att hårddiskarna som omfattar import- eller exportjobbet har levererats till Microsofts datacenter.
Den kan också användas för att avbryta ett befintligt jobb.

## SYNTAX

### UpdateExpanded (standard)
```
Update-AzImportExport -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AcceptLanguage <String>] [-BackupDriveManifest] [-CancelRequested] [-DeliveryPackageCarrierName <String>]
 [-DeliveryPackageDriveCount <Int32>] [-DeliveryPackageShipDate <String>]
 [-DeliveryPackageTrackingNumber <String>] [-DriveList <IDriveStatus[]>] [-LogLevel <String>]
 [-ReturnAddressCity <String>] [-ReturnAddressCountryOrRegion <String>] [-ReturnAddressEmail <String>]
 [-ReturnAddressPhone <String>] [-ReturnAddressPostalCode <String>] [-ReturnAddressRecipientName <String>]
 [-ReturnAddressStateOrProvince <String>] [-ReturnAddressStreetAddress1 <String>]
 [-ReturnAddressStreetAddress2 <String>] [-ReturnShippingCarrierAccountNumber <String>]
 [-ReturnShippingCarrierName <String>] [-State <String>] [-Tag <IUpdateJobParametersTags>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### UpdateViaIdentityExpanded
```
Update-AzImportExport -InputObject <IImportExportIdentity> [-AcceptLanguage <String>] [-BackupDriveManifest]
 [-CancelRequested] [-DeliveryPackageCarrierName <String>] [-DeliveryPackageDriveCount <Int32>]
 [-DeliveryPackageShipDate <String>] [-DeliveryPackageTrackingNumber <String>] [-DriveList <IDriveStatus[]>]
 [-LogLevel <String>] [-ReturnAddressCity <String>] [-ReturnAddressCountryOrRegion <String>]
 [-ReturnAddressEmail <String>] [-ReturnAddressPhone <String>] [-ReturnAddressPostalCode <String>]
 [-ReturnAddressRecipientName <String>] [-ReturnAddressStateOrProvince <String>]
 [-ReturnAddressStreetAddress1 <String>] [-ReturnAddressStreetAddress2 <String>]
 [-ReturnShippingCarrierAccountNumber <String>] [-ReturnShippingCarrierName <String>] [-State <String>]
 [-Tag <IUpdateJobParametersTags>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## BESKRIVNING
Uppdaterar specifika egenskaper för ett jobb.
Du kan anropa den här åtgärden om du vill meddela import-/exporttjänsten att hårddiskarna som omfattar import- eller exportjobbet har levererats till Microsofts datacenter.
Den kan också användas för att avbryta ett befintligt jobb.

## EXEMPEL

### Exempel 1: Uppdatera ImportExport-jobbet efter resursgrupp och servernamn
```powershell
PS C:\> Update-AzImportExport -Name test-job -ResourceGroupName ImportTestRG -DeliveryPackageCarrierName pwsh -DeliveryPackageTrackingNumber pwsh20200000
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

Den här cmdleten uppdaterar ImportExport-jobbet efter resursgrupp och servernamn.

### Exempel 2: Uppdatera importexportjobbet efter identitet.
```powershell
PS C:\> Get-AzImportExport -Name test-job -ResourceGroupName ImportTestRG | Update-AzImportExport -CancelRequested
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

Den här cmdleten uppdaterar ImportExport-jobbet efter identitet.

## PARAMETERS

### -AcceptLanguage
Anger det valda språket för svaret.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BackupDriveManifest
Anger om manifestfilerna på enheterna ska kopieras för att blockera blobbar.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CancelRequested
Om det anges måste värdet vara sant.
Tjänsten försöker avbryta jobbet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Autentiseringsuppgifter, konto, klientorganisation och prenumeration som används för kommunikation med Azure.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeliveryPackageCarrierName
Namnet på den operatör som används för att skicka in import- eller exportenheterna.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeliveryPackageDriveCount
Antalet enheter som ingår i paketet.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeliveryPackageShipDate
Datumet då paketet levererades.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeliveryPackageTrackingNumber
Spårningsnumret för paketet.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DriveList
Lista över enheter som utgör jobbet.
Skapa genom att gå till avsnittet ANTECKNINGAR för DRIVELIST-egenskaper och skapa en hash-tabell.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IDriveStatus[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Identitetsparameter att skapa finns i avsnittet ANTECKNINGAR för INPUTOBJECT-egenskaper och skapa en hash-tabell.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -LogLevel
Anger om felloggning eller utförlig loggning är aktiverat.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Namnet på import-/exportjobbet.

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: JobName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Resursgruppnamnet identifierar unikt resursgruppen i användarprenumerationen.

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReturnAddressCity
Ortnamnet som ska användas när du returnerar hårddiskarna.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReturnAddressCountryOrRegion
Det land eller den region som ska användas när du returnerar hårddiskarna.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReturnAddressEmail
E-postadressen till mottagaren av de returnerade diskarna.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReturnAddressPhone
Telefonnumret till mottagaren av de returnerade diskarna.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReturnAddressPostalCode
Postnumret som ska användas för att returnera hårddiskarna.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReturnAddressRecipientName
Namnet på mottagaren som får hårddiskarna när de returneras.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReturnAddressStateOrProvince
Den delstat eller provins som ska användas när du returnerar hårddiskarna.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReturnAddressStreetAddress1
Den första raden i gatuadressen som ska användas när du returnerar diskarna.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReturnAddressStreetAddress2
Den andra raden i gatuadressen som ska användas när du returnerar hårddiskarna.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReturnShippingCarrierAccountNumber
Kundens kontonummer hos operatören.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReturnShippingCarrierName
Transportföretagets namn.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Delstat
Om det anges måste värdet vara Leverans, vilket anger för import-/exporttjänsten att paketet för jobbet har levererats.
Egenskaperna ReturnAddress och DeliveryPackage måste ha angetts antingen i denna begäran eller i en tidigare begäran, annars misslyckas begäran.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
Azure-användarens prenumerations-ID.

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tag
Anger de taggar som ska tilldelas till jobbet

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IUpdateJobParametersTags
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Bekräfta
Frågar dig om bekräftelse innan du kör cmdleten.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Visar vad som skulle hända om cmdleten körs.
Cmdleten körs inte.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INDATA

### Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity

## UTDATA

### Microsoft.Azure.PowerShell.cmdlets.ImportExport.Models.Api20161101.IResponse

## ANTECKNINGAR

ALIAS

KOMPLEXA PARAMETEREGENSKAPER

Skapa de parametrar som beskrivs nedan genom att skapa en hash-tabell som innehåller rätt egenskaper. Om du vill ha information om hash-tabeller kör du Get-Help about_Hash_Tables.


DRIVELIST <IDriveStatus[]>: Lista över enheter som utgör jobbet.
  - `[BitLockerKey <String>]`: BitLocker-nyckeln som används för att kryptera enheten.
  - `[BytesSucceeded <Int64?>]`: Bytet överfördes för enheten.
  - `[CopyStatus <String>]`: Detaljerad status för dataöverföringsprocessen. Det här fältet returneras inte i svaret förrän enheten är i överföringstillståndet.
  - `[DriveHeaderHash <String>]`: Hash-värdet för enhetsrubriken.
  - `[DriveId <String>]`: Enhetens maskinvaruserienummer, utan blanksteg.
  - `[ErrorLogUri <String>]`: En URI som pekar på blobben som innehåller felloggen för dataöverföringsåtgärden.
  - `[ManifestFile <String>]`: Den relativa sökvägen till manifestfilen på enheten. 
  - `[ManifestHash <String>]`: Base16-kodad MD5-hash för manifestfilen på enheten.
  - `[ManifestUri <String>]`: En URI som pekar på blobben som innehåller manifestfilen för enheten. 
  - `[PercentComplete <Int32?>]`: Procent slutfört för enheten. 
  - `[State <DriveState?>]`: Enhetens aktuella status. 
  - `[VerboseLogUri <String>]`: En URI som pekar på blobben som innehåller den utförliga loggen för dataöverföringsåtgärden. 

INPUTOBJECT <IImportExportIdentity> : Identity Parameter
  - `[Id <String>]`: Resursidentitetssökväg
  - `[JobName <String>]`: Namnet på import-/exportjobbet.
  - `[LocationName <String>]`: Platsens namn. Till exempel Väst-USA eller WestUs.
  - `[ResourceGroupName <String>]`: Resursgruppsnamnet identifierar unikt resursgruppen i användarprenumerationen.
  - `[SubscriptionId <String>]`: Azure-användarens prenumerations-ID.

## RELATERADE LÄNKAR

