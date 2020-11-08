---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azmanagedhsmkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzManagedHsmKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzManagedHsmKey.md
ms.openlocfilehash: 89238992b99d86cdd56337a3002167be9c0d78d0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94273463"
---
# <span data-ttu-id="ca952-101">Add-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="ca952-101">Add-AzManagedHsmKey</span></span>

## <span data-ttu-id="ca952-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ca952-102">SYNOPSIS</span></span>
<span data-ttu-id="ca952-103">Skapar en Key i en hanterad HSM eller importerar en till en hanterad HSM.</span><span class="sxs-lookup"><span data-stu-id="ca952-103">Creates a key in a managed HSM or imports a key into a managed HSM.</span></span>

## <span data-ttu-id="ca952-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ca952-104">SYNTAX</span></span>

### <span data-ttu-id="ca952-105">InteractiveCreate (standard)</span><span class="sxs-lookup"><span data-stu-id="ca952-105">InteractiveCreate (Default)</span></span>
```
Add-AzManagedHsmKey [-HsmName] <String> [-Name] <String> -KeyType <String> [-CurveName <String>] [-Disable]
 [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca952-106">InteractiveImport</span><span class="sxs-lookup"><span data-stu-id="ca952-106">InteractiveImport</span></span>
```
Add-AzManagedHsmKey [-HsmName] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-CurveName <String>] [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>]
 [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ca952-107">InputObjectCreate</span><span class="sxs-lookup"><span data-stu-id="ca952-107">InputObjectCreate</span></span>
```
Add-AzManagedHsmKey [-InputObject] <PSManagedHsm> [-Name] <String> -KeyType <String> [-CurveName <String>]
 [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>]
 [-Size <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca952-108">InputObjectImport</span><span class="sxs-lookup"><span data-stu-id="ca952-108">InputObjectImport</span></span>
```
Add-AzManagedHsmKey [-InputObject] <PSManagedHsm> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-CurveName <String>] [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>]
 [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ca952-109">ResourceIdCreate</span><span class="sxs-lookup"><span data-stu-id="ca952-109">ResourceIdCreate</span></span>
```
Add-AzManagedHsmKey [-ResourceId] <String> [-Name] <String> -KeyType <String> [-CurveName <String>] [-Disable]
 [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca952-110">ResourceIdImport</span><span class="sxs-lookup"><span data-stu-id="ca952-110">ResourceIdImport</span></span>
```
Add-AzManagedHsmKey [-ResourceId] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-CurveName <String>] [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>]
 [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ca952-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ca952-111">DESCRIPTION</span></span>
<span data-ttu-id="ca952-112">Cmdleten **Add-AzManagedHsmKey** skapar en Key i en hanterad HSM i Azure Managed HSM eller importerar en i en hanterad HSM.</span><span class="sxs-lookup"><span data-stu-id="ca952-112">The **Add-AzManagedHsmKey** cmdlet creates a key in a managed HSM in Azure Managed Hsm or imports a key into a managed HSM.</span></span>
<span data-ttu-id="ca952-113">Använd denna cmdlet för att lägga till nycklar på något av följande sätt:</span><span class="sxs-lookup"><span data-stu-id="ca952-113">Use this cmdlet to add keys by using any of the following methods:</span></span>
- <span data-ttu-id="ca952-114">Skapa en nycklar med standardattribut</span><span class="sxs-lookup"><span data-stu-id="ca952-114">Create a key with default key attributes</span></span>
- <span data-ttu-id="ca952-115">Skapa en nycklar med angivna nyckelattribut</span><span class="sxs-lookup"><span data-stu-id="ca952-115">Create a key with given key attributes</span></span>
- <span data-ttu-id="ca952-116">Importera en från en. pfx-fil på datorn.</span><span class="sxs-lookup"><span data-stu-id="ca952-116">Import a key from a .pfx file on your computer.</span></span>
<span data-ttu-id="ca952-117">Du kan ange nyckelattribut eller acceptera standardinställningar för de här åtgärderna.</span><span class="sxs-lookup"><span data-stu-id="ca952-117">For any of these operations, you can provide key attributes or accept default settings.</span></span>
<span data-ttu-id="ca952-118">Om du skapar eller importerar en nycklar som har samma namn som en befintlig nycklar i en hanterad HSM uppdateras den ursprungliga tangenten med de värden som du anger för den nya.</span><span class="sxs-lookup"><span data-stu-id="ca952-118">If you create or import a key that has the same name as an existing key in your managed HSM, the original key is updated with the values that you specify for the new key.</span></span> <span data-ttu-id="ca952-119">Du kan komma åt föregående värden med den version-specifika URI för den versionen av den här tangenten.</span><span class="sxs-lookup"><span data-stu-id="ca952-119">You can access the previous values by using the version-specific URI for that version of the key.</span></span> <span data-ttu-id="ca952-120">Mer information om nyckel versioner och URI-strukturen finns i [om nycklar och hemligheter](http://go.microsoft.com/fwlink/?linkid=518560) i den HANTERAde HSM-dokumentationen.</span><span class="sxs-lookup"><span data-stu-id="ca952-120">To learn about key versions and the URI structure, see [About Keys and Secrets](http://go.microsoft.com/fwlink/?linkid=518560) in the Managed HSM REST API documentation.</span></span>

## <span data-ttu-id="ca952-121">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ca952-121">EXAMPLES</span></span>

### <span data-ttu-id="ca952-122">Exempel 1: skapa en RSA-HSM-tangenten</span><span class="sxs-lookup"><span data-stu-id="ca952-122">Example 1: Create a RSA-HSM key</span></span>
```powershell
PS C:\> Add-AzManagedHsmKey -HsmName testmhsm -Name testkey -KeyType RSA

Vault/HSM Name : testmhsm
Name           : testkey
Version        : xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
Id             : https://bezmhsm.managedhsm.azure.net:443/keys/testkey/xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
Enabled        : True
Expires        :
Not Before     :
Created        : 10/14/2020 7:55:43 AM
Updated        : 10/14/2020 7:55:43 AM
Recovery Level : Recoverable+Purgeable
Tags           :
```

<span data-ttu-id="ca952-123">Det här kommandot skapar en RSA-HSM-Key med namnet testkey i testkey med namnet testmhsm.</span><span class="sxs-lookup"><span data-stu-id="ca952-123">This command creates a RSA-HSM key named testkey in the managed HSM testkey named testmhsm.</span></span>

### <span data-ttu-id="ca952-124">Exempel 2: skapa en EG-HSM-tangenten</span><span class="sxs-lookup"><span data-stu-id="ca952-124">Example 2: Create a EC-HSM key</span></span>
```powershell
PS C:\> Add-AzManagedHsmKey -HsmName testmhsm -Name testkey -KeyType EC -CurveName P-256

Vault/HSM Name : testmhsm
Name           : testkey
Version        : xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
Id             : https://bezmhsm.managedhsm.azure.net:443/keys/testkey/xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
Enabled        : True
Expires        :
Not Before     :
Created        : 10/14/2020 8:06:26 AM
Updated        : 10/14/2020 8:06:26 AM
Recovery Level : Recoverable+Purgeable
Tags           :
```

<span data-ttu-id="ca952-125">Det här kommandot skapar en EC-HSM-knapp med namnet testkey med hjälp av en P-256-kurva i den hanterade HSM testkey som heter testmhsm.</span><span class="sxs-lookup"><span data-stu-id="ca952-125">This command creates a EC-HSM key named testkey using P-256 curve in the managed HSM testkey named testmhsm.</span></span>

### <span data-ttu-id="ca952-126">Exempel 3: skapa en okt-HSM-nycklar med icke-standardvärden</span><span class="sxs-lookup"><span data-stu-id="ca952-126">Example 3: Create a oct-HSM key with non-default values</span></span>
```powershell
PS C:\> $KeyOperations = 'decrypt', 'verify'
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $NotBefore = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = "true"}
PS C:\> Add-AzManagedHsmKey -HsmName testmhsm -Name testkey -KeyType oct -Expires $Expires -NotBefore $NotBefore -KeyOps $KeyOperations -Disable -Tag $Tags

Vault/HSM Name : testmhsm
Name           : testkey
Version        : xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
Id             : https://bezmhsm.managedhsm.azure.net:443/keys/testkey/xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
Enabled        : False
Expires        : 10/14/2022 8:13:29 AM
Not Before     : 10/14/2020 8:13:33 AM
Created        : 10/14/2020 8:14:01 AM
Updated        : 10/14/2020 8:14:01 AM
Recovery Level : Recoverable+Purgeable
Tags           : Name        Value
                 Severity    high
                 Accounting  true
```

<span data-ttu-id="ca952-127">Med det första kommandot lagras värdena dekryptera och verifiera i $KeyOperations variabeln.</span><span class="sxs-lookup"><span data-stu-id="ca952-127">The first command stores the values decrypt and verify in the $KeyOperations variable.</span></span>
<span data-ttu-id="ca952-128">Det andra kommandot skapar ett **datetime** -objekt, DEFINIERAT i UTC, med hjälp av cmdleten **Get-date** .</span><span class="sxs-lookup"><span data-stu-id="ca952-128">The second command creates a **DateTime** object, defined in UTC, by using the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="ca952-129">Detta objekt anger en tid två år framåt i tiden.</span><span class="sxs-lookup"><span data-stu-id="ca952-129">That object specifies a time two years in the future.</span></span> <span data-ttu-id="ca952-130">I kommandot lagras datumet i $Expires variabel.</span><span class="sxs-lookup"><span data-stu-id="ca952-130">The command stores that date in the $Expires variable.</span></span> <span data-ttu-id="ca952-131">Om du vill ha mer information skriver du `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="ca952-131">For more information, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="ca952-132">Det tredje kommandot skapar ett **datetime** -objekt med hjälp av cmdleten **Get-date** .</span><span class="sxs-lookup"><span data-stu-id="ca952-132">The third command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="ca952-133">Det objektet anger den aktuella UTC-tiden.</span><span class="sxs-lookup"><span data-stu-id="ca952-133">That object specifies current UTC time.</span></span> <span data-ttu-id="ca952-134">I kommandot lagras datumet i $NotBefore variabel.</span><span class="sxs-lookup"><span data-stu-id="ca952-134">The command stores that date in the $NotBefore variable.</span></span>
<span data-ttu-id="ca952-135">Med kommandot slut skapas en Key som heter testkey som är en lands-HSM-tangenten.</span><span class="sxs-lookup"><span data-stu-id="ca952-135">The final command creates a key named testkey that is an oct-HSM key.</span></span> <span data-ttu-id="ca952-136">Kommandot anger värden för tillåtna operationer som lagras $KeyOperations.</span><span class="sxs-lookup"><span data-stu-id="ca952-136">The command specifies values for allowed key operations stored $KeyOperations.</span></span> <span data-ttu-id="ca952-137">Kommandot anger tider för parametrarna *Expires* och *NotBefore* som skapats i föregående kommandon och taggar för hög allvarlighets grad och det.</span><span class="sxs-lookup"><span data-stu-id="ca952-137">The command specifies times for the *Expires* and *NotBefore* parameters created in the previous commands, and tags for high severity and IT.</span></span> <span data-ttu-id="ca952-138">Den nya knappen är inaktive rad.</span><span class="sxs-lookup"><span data-stu-id="ca952-138">The new key is disabled.</span></span> <span data-ttu-id="ca952-139">Du kan aktivera det med hjälp av cmdleten **Update-AzManagedHsmKey** .</span><span class="sxs-lookup"><span data-stu-id="ca952-139">You can enable it by using the **Update-AzManagedHsmKey** cmdlet.</span></span>

## <span data-ttu-id="ca952-140">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ca952-140">PARAMETERS</span></span>

### <span data-ttu-id="ca952-141">-CurveName</span><span class="sxs-lookup"><span data-stu-id="ca952-141">-CurveName</span></span>
<span data-ttu-id="ca952-142">Anger kurv namnet på Elliptic Curve Cryptography, det här värdet är giltigt när en typ är EC.</span><span class="sxs-lookup"><span data-stu-id="ca952-142">Specifies the curve name of elliptic curve cryptography, this value is valid when KeyType is EC.</span></span>

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

### <span data-ttu-id="ca952-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca952-143">-DefaultProfile</span></span>
<span data-ttu-id="ca952-144">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ca952-144">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca952-145">-Inaktivera</span><span class="sxs-lookup"><span data-stu-id="ca952-145">-Disable</span></span>
<span data-ttu-id="ca952-146">Visar att den aktuella knappen är inaktive rad.</span><span class="sxs-lookup"><span data-stu-id="ca952-146">Indicates that the key you are adding is set to an initial state of disabled.</span></span>
<span data-ttu-id="ca952-147">Alla försök att använda den här knappen fungerar inte.</span><span class="sxs-lookup"><span data-stu-id="ca952-147">Any attempt to use the key will fail.</span></span>
<span data-ttu-id="ca952-148">Använd den här parametern om du har förinstallerat de nycklar du tänker aktivera senare.</span><span class="sxs-lookup"><span data-stu-id="ca952-148">Use this parameter if you are preloading keys that you intend to enable later.</span></span>

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

### <span data-ttu-id="ca952-149">-Upphör</span><span class="sxs-lookup"><span data-stu-id="ca952-149">-Expires</span></span>
<span data-ttu-id="ca952-150">Anger värdet för förfallo tid i UTC.</span><span class="sxs-lookup"><span data-stu-id="ca952-150">Specifies the expiration time of the key in UTC.</span></span>
<span data-ttu-id="ca952-151">Om det inte anges upphör inte nycklar att gälla.</span><span class="sxs-lookup"><span data-stu-id="ca952-151">If not specified, key will not expire.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca952-152">-HsmName</span><span class="sxs-lookup"><span data-stu-id="ca952-152">-HsmName</span></span>
<span data-ttu-id="ca952-153">HSM-namn.</span><span class="sxs-lookup"><span data-stu-id="ca952-153">HSM name.</span></span> <span data-ttu-id="ca952-154">Cmdlet konstruerar FQDN för en hanterad HSM baserat på namnet och den valda miljön.</span><span class="sxs-lookup"><span data-stu-id="ca952-154">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveCreate, InteractiveImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca952-155">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ca952-155">-InputObject</span></span>
<span data-ttu-id="ca952-156">HSM-objekt.</span><span class="sxs-lookup"><span data-stu-id="ca952-156">HSM object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: InputObjectCreate, InputObjectImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ca952-157">-KeyFilePassword</span><span class="sxs-lookup"><span data-stu-id="ca952-157">-KeyFilePassword</span></span>
<span data-ttu-id="ca952-158">Lösen ord för den lokala filen som innehåller det nyckel material som ska importeras.</span><span class="sxs-lookup"><span data-stu-id="ca952-158">Password of the local file containing the key material to be imported.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: InteractiveImport, InputObjectImport, ResourceIdImport
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca952-159">-Fil Sök väg</span><span class="sxs-lookup"><span data-stu-id="ca952-159">-KeyFilePath</span></span>
<span data-ttu-id="ca952-160">Sökväg till den lokala filen som innehåller det nyckel material som ska importeras.</span><span class="sxs-lookup"><span data-stu-id="ca952-160">Path to the local file containing the key material to be imported.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveImport, InputObjectImport, ResourceIdImport
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca952-161">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="ca952-161">-KeyOps</span></span>
<span data-ttu-id="ca952-162">Vilka operationer som kan utföras med tangenten.</span><span class="sxs-lookup"><span data-stu-id="ca952-162">The operations that can be performed with the key.</span></span>
<span data-ttu-id="ca952-163">Om det inte visas kan alla operationer utföras.</span><span class="sxs-lookup"><span data-stu-id="ca952-163">If not present, all operations can be performed.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca952-164">-Värdetyp</span><span class="sxs-lookup"><span data-stu-id="ca952-164">-KeyType</span></span>
<span data-ttu-id="ca952-165">Anger Key-typen för den här tangenten.</span><span class="sxs-lookup"><span data-stu-id="ca952-165">Specifies the key type of this key.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveCreate, InputObjectCreate, ResourceIdCreate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca952-166">-Namn</span><span class="sxs-lookup"><span data-stu-id="ca952-166">-Name</span></span>
<span data-ttu-id="ca952-167">Namn på knappen.</span><span class="sxs-lookup"><span data-stu-id="ca952-167">Key name.</span></span>
<span data-ttu-id="ca952-168">Cmdlet konstruerar FQDN för en Key från Managed HSM-namn, markerat miljö-och namn för tillfället.</span><span class="sxs-lookup"><span data-stu-id="ca952-168">Cmdlet constructs the FQDN of a key from managed HSM name, currently selected environment and key name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca952-169">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="ca952-169">-NotBefore</span></span>
<span data-ttu-id="ca952-170">UTC-tiden innan tangenten kan användas.</span><span class="sxs-lookup"><span data-stu-id="ca952-170">The UTC time before which the key can't be used.</span></span>
<span data-ttu-id="ca952-171">Om inget anges är det inga begränsningar.</span><span class="sxs-lookup"><span data-stu-id="ca952-171">If not specified, there is no limitation.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca952-172">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ca952-172">-ResourceId</span></span>
<span data-ttu-id="ca952-173">HSM-resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="ca952-173">HSM Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdCreate, ResourceIdImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca952-174">-Storlek</span><span class="sxs-lookup"><span data-stu-id="ca952-174">-Size</span></span>
<span data-ttu-id="ca952-175">RSA-nyckelbaserad storlek, i bitar.</span><span class="sxs-lookup"><span data-stu-id="ca952-175">RSA key size, in bits.</span></span>
<span data-ttu-id="ca952-176">Om det inte anges ger tjänsten ett säkert standardvärde.</span><span class="sxs-lookup"><span data-stu-id="ca952-176">If not specified, the service will provide a safe default.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: InteractiveCreate, InputObjectCreate, ResourceIdCreate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca952-177">-Tagg</span><span class="sxs-lookup"><span data-stu-id="ca952-177">-Tag</span></span>
<span data-ttu-id="ca952-178">En hash-produkt som representerar viktiga taggar.</span><span class="sxs-lookup"><span data-stu-id="ca952-178">A hashtable representing key tags.</span></span>

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

### <span data-ttu-id="ca952-179">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ca952-179">-Confirm</span></span>
<span data-ttu-id="ca952-180">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ca952-180">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca952-181">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca952-181">-WhatIf</span></span>
<span data-ttu-id="ca952-182">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ca952-182">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca952-183">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ca952-183">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca952-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca952-184">CommonParameters</span></span>
<span data-ttu-id="ca952-185">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca952-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca952-186">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ca952-186">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca952-187">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ca952-187">INPUTS</span></span>

### <span data-ttu-id="ca952-188">Microsoft. Azure. commands. valv. Models. PSManagedHsm</span><span class="sxs-lookup"><span data-stu-id="ca952-188">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

### <span data-ttu-id="ca952-189">System. String</span><span class="sxs-lookup"><span data-stu-id="ca952-189">System.String</span></span>

## <span data-ttu-id="ca952-190">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ca952-190">OUTPUTS</span></span>

### <span data-ttu-id="ca952-191">Microsoft. Azure. commands. valv. Models. PSManagedHsm</span><span class="sxs-lookup"><span data-stu-id="ca952-191">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

## <span data-ttu-id="ca952-192">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ca952-192">NOTES</span></span>

## <span data-ttu-id="ca952-193">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ca952-193">RELATED LINKS</span></span>

[<span data-ttu-id="ca952-194">Säkerhets kopiering-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="ca952-194">Backup-AzManagedHsmKey</span></span>](./Backup-AzManagedHsmKey.md)

[<span data-ttu-id="ca952-195">Get-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="ca952-195">Get-AzManagedHsmKey</span></span>](./Get-AzManagedHsmKey.md)

[<span data-ttu-id="ca952-196">Remove-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="ca952-196">Remove-AzManagedHsmKey</span></span>](./Remove-AzManagedHsmKey.md)

[<span data-ttu-id="ca952-197">Ångra-AzManagedHsmKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="ca952-197">Undo-AzManagedHsmKeyRemoval</span></span>](./Undo-AzManagedHsmKeyRemoval.md)

[<span data-ttu-id="ca952-198">Update-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="ca952-198">Update-AzManagedHsmKey</span></span>](./Update-AzManagedHsmKey.md)

[<span data-ttu-id="ca952-199">Återställ-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="ca952-199">Restore-AzManagedHsmKey</span></span>](./Restore-AzManagedHsmKey.md)
