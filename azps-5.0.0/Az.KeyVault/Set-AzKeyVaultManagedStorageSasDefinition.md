---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultmanagedstoragesasdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: ff73d5db0b16d7176b9c49aa6e70bc13fc9f3fba
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94263009"
---
# <span data-ttu-id="3e6fc-101">Set-AzKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="3e6fc-101">Set-AzKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="3e6fc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3e6fc-102">SYNOPSIS</span></span>
<span data-ttu-id="3e6fc-103">Ställer in en säkerhets beskrivning för en delad åtkomst (SAS) med ett huvud valv för ett visst offentligt hanterat Azure Storage-konto.</span><span class="sxs-lookup"><span data-stu-id="3e6fc-103">Sets a Shared Access Signature (SAS) definition with Key Vault for a given Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="3e6fc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3e6fc-104">SYNTAX</span></span>

### <span data-ttu-id="3e6fc-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="3e6fc-105">Default (Default)</span></span>
```
Set-AzKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-TemplateUri] <String> [-SasType] <String> [-Disable] [-Tag <Hashtable>] -ValidityPeriod <TimeSpan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e6fc-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="3e6fc-106">ByInputObject</span></span>
```
Set-AzKeyVaultManagedStorageSasDefinition [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [-Name] <String> [-TemplateUri] <String> [-SasType] <String> [-Disable] [-Tag <Hashtable>]
 -ValidityPeriod <TimeSpan> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3e6fc-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3e6fc-107">DESCRIPTION</span></span>
<span data-ttu-id="3e6fc-108">Ställer in en säkerhets beskrivning för en signatur (SAS) med ett angivet Azure Storage-konto för viktiga valv.</span><span class="sxs-lookup"><span data-stu-id="3e6fc-108">Sets a Shared Access Signature (SAS) definition with a given Key Vault managed Azure Storage Account.</span></span> <span data-ttu-id="3e6fc-109">Detta anger också en hemlighet som kan användas för att hämta SAS-token per denna SAS-definition.</span><span class="sxs-lookup"><span data-stu-id="3e6fc-109">This also sets a secret which can be used to get the SAS token per this SAS definition.</span></span>
<span data-ttu-id="3e6fc-110">SAS-token genereras med de här parametrarna och den aktiva nyckeln för det hanterade Azure Storage-kontot för Key valv.</span><span class="sxs-lookup"><span data-stu-id="3e6fc-110">SAS token is generated using these parameters and the active key of the Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="3e6fc-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3e6fc-111">EXAMPLES</span></span>

### <span data-ttu-id="3e6fc-112">Exempel 1: Ange en SAS-definition för konto typer och få en aktuell SAS-token baserad på den</span><span class="sxs-lookup"><span data-stu-id="3e6fc-112">Example 1: Set an account-type SAS definition, and obtain a current SAS token based on it</span></span>
```powershell
PS C:\> $sa = Get-AzStorageAccount -Name mysa -ResourceGroupName myrg
PS C:\> $kv = Get-AzKeyVault -VaultName mykv
PS C:\> Add-AzKeyVaultManagedStorageAccount -VaultName $kv.VaultName -AccountName $sa.StorageAccountName -AccountResourceId $sa.Id -ActiveKeyName key1 -RegenerationPeriod ([System.Timespan]::FromDays(180))
PS C:\> $sctx = New-AzStorageContext -StorageAccountName $sa.StorageAccountName -Protocol Https -StorageAccountKey Key1
PS C:\> $start = [System.DateTime]::Now.AddDays(-1)
PS C:\> $end = [System.DateTime]::Now.AddMonths(1)
PS C:\> $at = New-AzStorageAccountSasToken -Service blob,file,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup" -Protocol HttpsOnly -StartTime $start -ExpiryTime $end -Context $sctx
PS C:\> $sas = Set-AzKeyVaultManagedStorageSasDefinition -AccountName $sa.StorageAccountName -VaultName $kv.VaultName -Name accountsas -TemplateUri $at -SasType 'account' -ValidityPeriod ([System.Timespan]::FromDays(30))
PS C:\> Get-AzKeyVaultSecret -VaultName $kv.VaultName -Name $sas.Sid.Substring($sas.Sid.LastIndexOf('/')+1)
```

<span data-ttu-id="3e6fc-113">Anger ett konto för SAS-definitionen för konton på ett valv-hanterat lagrings konto ' mysa ' i valv ' mykv '.</span><span class="sxs-lookup"><span data-stu-id="3e6fc-113">Sets an account SAS definition 'accountsas' on a KeyVault-managed storage account 'mysa' in vault 'mykv'.</span></span> <span data-ttu-id="3e6fc-114">Ordningen ovan gör följande:</span><span class="sxs-lookup"><span data-stu-id="3e6fc-114">Specifically, the sequence above performs the following:</span></span>
  - <span data-ttu-id="3e6fc-115">hämtar ett (befintligt) lagrings konto</span><span class="sxs-lookup"><span data-stu-id="3e6fc-115">gets a (pre-existing) storage account</span></span>
  - <span data-ttu-id="3e6fc-116">hämtar ett (befintligt) huvud valv</span><span class="sxs-lookup"><span data-stu-id="3e6fc-116">gets a (pre-existing) key vault</span></span>
  - <span data-ttu-id="3e6fc-117">lägger till ett valv-hanterat lagrings konto i valvet, ställer in KEY1 som aktiv-nycklar och med en återställnings period på 180 dagar</span><span class="sxs-lookup"><span data-stu-id="3e6fc-117">adds a KeyVault-managed storage account to the vault, setting Key1 as the active key, and with a regeneration period of 180 days</span></span>
  - <span data-ttu-id="3e6fc-118">anger en lagrings kontext för det angivna lagrings kontot med KEY1</span><span class="sxs-lookup"><span data-stu-id="3e6fc-118">sets a storage context for the specified storage account, with Key1</span></span>
  - <span data-ttu-id="3e6fc-119">skapar ett konto SAS-token för tjänster, fil, tabell och kö, för resurs typ tjänst, behållare och objekt med alla behörigheter, över https och med angivna start-och slutdatum</span><span class="sxs-lookup"><span data-stu-id="3e6fc-119">creates an account SAS token for services Blob, File, Table and Queue, for resource types Service, Container and Object, with all permissions, over https and with the specified start and end dates</span></span>
  - <span data-ttu-id="3e6fc-120">anger en säkerhets definition för ett nyckel valv som hanteras i ett valv i valvet med mallen URI som den SAS-token som skapades ovan, av SAS-typ "konto" och giltigt i 30 dagar</span><span class="sxs-lookup"><span data-stu-id="3e6fc-120">sets a KeyVault-managed storage SAS definition in the vault, with the template uri as the SAS token created above, of SAS type 'account' and valid for 30 days</span></span>
  - <span data-ttu-id="3e6fc-121">hämtar den faktiska åtkomst-token från den nyckel valv hemlighet som motsvarar SAS-definitionen</span><span class="sxs-lookup"><span data-stu-id="3e6fc-121">retrieves the actual access token from the KeyVault secret corresponding to the SAS definition</span></span>

## <span data-ttu-id="3e6fc-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3e6fc-122">PARAMETERS</span></span>

### <span data-ttu-id="3e6fc-123">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3e6fc-123">-AccountName</span></span>
<span data-ttu-id="3e6fc-124">Namn på hanterat lagrings konto för viktiga valv.</span><span class="sxs-lookup"><span data-stu-id="3e6fc-124">Key Vault managed storage account name.</span></span> <span data-ttu-id="3e6fc-125">Cmdlet konstruerar FQDN för ett hanterat lagrings konto namn från valv namn, valt miljö-och manged.</span><span class="sxs-lookup"><span data-stu-id="3e6fc-125">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e6fc-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e6fc-126">-DefaultProfile</span></span>
<span data-ttu-id="3e6fc-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="3e6fc-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e6fc-128">-Inaktivera</span><span class="sxs-lookup"><span data-stu-id="3e6fc-128">-Disable</span></span>
<span data-ttu-id="3e6fc-129">Inaktiverar användning av SAS-definition för generering av SAS-token.</span><span class="sxs-lookup"><span data-stu-id="3e6fc-129">Disables the use of sas definition for generation of sas token.</span></span>

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

### <span data-ttu-id="3e6fc-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3e6fc-130">-InputObject</span></span>
<span data-ttu-id="3e6fc-131">ManagedStorageAccount-objekt.</span><span class="sxs-lookup"><span data-stu-id="3e6fc-131">ManagedStorageAccount object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3e6fc-132">-Namn</span><span class="sxs-lookup"><span data-stu-id="3e6fc-132">-Name</span></span>
<span data-ttu-id="3e6fc-133">Namn på lagrings-sa.</span><span class="sxs-lookup"><span data-stu-id="3e6fc-133">Storage sas definition name.</span></span> <span data-ttu-id="3e6fc-134">Cmdlet konstruerar FQDN-namnet på en lagrings-säkerhets Association från ett valv namn, för närvarande valda miljö-, lagrings konto namn och SAS-namn.</span><span class="sxs-lookup"><span data-stu-id="3e6fc-134">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SasDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e6fc-135">-SasType</span><span class="sxs-lookup"><span data-stu-id="3e6fc-135">-SasType</span></span>
<span data-ttu-id="3e6fc-136">Säkerhets Association för lagring.</span><span class="sxs-lookup"><span data-stu-id="3e6fc-136">Storage SAS type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e6fc-137">-Tagg</span><span class="sxs-lookup"><span data-stu-id="3e6fc-137">-Tag</span></span>
<span data-ttu-id="3e6fc-138">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="3e6fc-138">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="3e6fc-139">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="3e6fc-139">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e6fc-140">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="3e6fc-140">-TemplateUri</span></span>
<span data-ttu-id="3e6fc-141">URI för definitions mal len lagrings Association med SAS.</span><span class="sxs-lookup"><span data-stu-id="3e6fc-141">Storage SAS definition template uri.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e6fc-142">-ValidityPeriod</span><span class="sxs-lookup"><span data-stu-id="3e6fc-142">-ValidityPeriod</span></span>
<span data-ttu-id="3e6fc-143">Giltighets tids period som används för att ange förfallo tiden för SAS-token från den tid då den genereras</span><span class="sxs-lookup"><span data-stu-id="3e6fc-143">Validity period that will get used to set the expiry time of sas token from the time it gets generated</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e6fc-144">-VaultName</span><span class="sxs-lookup"><span data-stu-id="3e6fc-144">-VaultName</span></span>
<span data-ttu-id="3e6fc-145">Valv namn.</span><span class="sxs-lookup"><span data-stu-id="3e6fc-145">Vault name.</span></span>
<span data-ttu-id="3e6fc-146">Cmdlet konstruerar FQDN för ett valv baserat på namnet och den valda miljön.</span><span class="sxs-lookup"><span data-stu-id="3e6fc-146">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e6fc-147">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3e6fc-147">-Confirm</span></span>
<span data-ttu-id="3e6fc-148">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3e6fc-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e6fc-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e6fc-149">-WhatIf</span></span>
<span data-ttu-id="3e6fc-150">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3e6fc-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e6fc-151">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3e6fc-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e6fc-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e6fc-152">CommonParameters</span></span>
<span data-ttu-id="3e6fc-153">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e6fc-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e6fc-154">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3e6fc-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e6fc-155">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3e6fc-155">INPUTS</span></span>

### <span data-ttu-id="3e6fc-156">Microsoft. Azure. commands. valv. Models. PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="3e6fc-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="3e6fc-157">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3e6fc-157">OUTPUTS</span></span>

### <span data-ttu-id="3e6fc-158">Microsoft. Azure. commands. valv. Models. PSKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="3e6fc-158">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="3e6fc-159">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3e6fc-159">NOTES</span></span>

## <span data-ttu-id="3e6fc-160">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3e6fc-160">RELATED LINKS</span></span>

[<span data-ttu-id="3e6fc-161">Azureâ € ofta ‹ RM. â € ofta ‹ keyâ € ofta ‹ valv</span><span class="sxs-lookup"><span data-stu-id="3e6fc-161">Azureâ€‹RM.â€‹Keyâ€‹Vault</span></span>](/powershell/module/az.keyvault/)
