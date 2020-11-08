---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azmanagedhsmkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzManagedHsmKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzManagedHsmKey.md
ms.openlocfilehash: 34bc2f074ee37dcf670e3e43ad647781b4d59e56
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94263034"
---
# <span data-ttu-id="a1990-101">Get-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="a1990-101">Get-AzManagedHsmKey</span></span>

## <span data-ttu-id="a1990-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a1990-102">SYNOPSIS</span></span>
<span data-ttu-id="a1990-103">Hämtar hanterade HSM-nycklar.</span><span class="sxs-lookup"><span data-stu-id="a1990-103">Gets Managed Hsm keys.</span></span>

## <span data-ttu-id="a1990-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a1990-104">SYNTAX</span></span>

### <span data-ttu-id="a1990-105">SpecifyHsmByHsmNameGetKeyWithoutConstraint (standard)</span><span class="sxs-lookup"><span data-stu-id="a1990-105">SpecifyHsmByHsmNameGetKeyWithoutConstraint (Default)</span></span>
```
Get-AzManagedHsmKey [-HsmName] <String> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a1990-106">SpecifyHsmByHsmNameGetKeyWithSpecifiedVersion</span><span class="sxs-lookup"><span data-stu-id="a1990-106">SpecifyHsmByHsmNameGetKeyWithSpecifiedVersion</span></span>
```
Get-AzManagedHsmKey [-HsmName] <String> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a1990-107">SpecifyHsmByHsmNameGetKeyIncludeAllVersions</span><span class="sxs-lookup"><span data-stu-id="a1990-107">SpecifyHsmByHsmNameGetKeyIncludeAllVersions</span></span>
```
Get-AzManagedHsmKey [-HsmName] <String> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a1990-108">SpecifyHsmByInputObjectGetKeyWithoutConstraint</span><span class="sxs-lookup"><span data-stu-id="a1990-108">SpecifyHsmByInputObjectGetKeyWithoutConstraint</span></span>
```
Get-AzManagedHsmKey [-InputObject] <PSManagedHsm> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a1990-109">SpecifyHsmByInputObjectGetKeyWithSpecifiedVersion</span><span class="sxs-lookup"><span data-stu-id="a1990-109">SpecifyHsmByInputObjectGetKeyWithSpecifiedVersion</span></span>
```
Get-AzManagedHsmKey [-InputObject] <PSManagedHsm> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a1990-110">SpecifyHsmByInputObjectGetKeyIncludeAllVersions</span><span class="sxs-lookup"><span data-stu-id="a1990-110">SpecifyHsmByInputObjectGetKeyIncludeAllVersions</span></span>
```
Get-AzManagedHsmKey [-InputObject] <PSManagedHsm> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a1990-111">SpecifyHsmByResourceIdGetKeyWithoutConstraint</span><span class="sxs-lookup"><span data-stu-id="a1990-111">SpecifyHsmByResourceIdGetKeyWithoutConstraint</span></span>
```
Get-AzManagedHsmKey [-ResourceId] <String> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a1990-112">SpecifyHsmByResourceIdGetKeyWithSpecifiedVersion</span><span class="sxs-lookup"><span data-stu-id="a1990-112">SpecifyHsmByResourceIdGetKeyWithSpecifiedVersion</span></span>
```
Get-AzManagedHsmKey [-ResourceId] <String> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a1990-113">SpecifyHsmByResourceIdGetKeyIncludeAllVersions</span><span class="sxs-lookup"><span data-stu-id="a1990-113">SpecifyHsmByResourceIdGetKeyIncludeAllVersions</span></span>
```
Get-AzManagedHsmKey [-ResourceId] <String> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1990-114">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a1990-114">DESCRIPTION</span></span>
<span data-ttu-id="a1990-115">Cmdleten **Get-AzManagedHsmKey** får Azure Managed HSM-knappar.</span><span class="sxs-lookup"><span data-stu-id="a1990-115">The **Get-AzManagedHsmKey** cmdlet gets Azure Managed Hsm keys.</span></span>
<span data-ttu-id="a1990-116">Denna cmdlet hämtar ett specifikt **Microsoft. Azure.-kommandon. valv** ...-paket eller en lista över alla **paket** -objekt i en hanterad HSM eller efter version.</span><span class="sxs-lookup"><span data-stu-id="a1990-116">This cmdlet gets a specific **Microsoft.Azure.Commands.KeyVault.Models.KeyBundle** or a list of all **KeyBundle** objects in a managed Hsm or by version.</span></span>

## <span data-ttu-id="a1990-117">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a1990-117">EXAMPLES</span></span>

### <span data-ttu-id="a1990-118">Exempel 1: Hämta alla nycklar i en hanterad HSM</span><span class="sxs-lookup"><span data-stu-id="a1990-118">Example 1: Get all the keys in a managed HSM</span></span>
```powershell
PS C:\> Get-AzManagedHsmKey -HsmName testmhsm
```

<span data-ttu-id="a1990-119">Valv/HSM-namn: testmhsm namn: testkey001-version: ID: https://testmhsm.managedhsm.azure.net:443/keys/testkey001 Enabled: true upphör: ej före: Skapad: 10/14/2020 3:39:16 har uppdaterats: 10/14/2020 3:39:16 am återställnings nivå: återtäckning + tömnings bar tagg:</span><span class="sxs-lookup"><span data-stu-id="a1990-119">Vault/HSM Name : testmhsm Name           : testkey001 Version        : Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey001 Enabled        : True Expires        : Not Before     : Created        : 10/14/2020 3:39:16 AM Updated        : 10/14/2020 3:39:16 AM Recovery Level : Recoverable+Purgeable Tags           :</span></span>

<span data-ttu-id="a1990-120">Valv/HSM-namn: testmhsm namn: testkey002-version: ID: https://testmhsm.managedhsm.azure.net:443/keys/testkey002 Enabled: false upphör: 10/14/2022 8:13:29 är inte före: 10/14/2020 8:13:33 am: 10/14/2020 8:14:01 har uppdaterats: 10/14/2020 8:14:01 am återställnings nivå: återställning + tömnings bar: namn värdes allvarlighets grad för stor redovisning sant</span><span class="sxs-lookup"><span data-stu-id="a1990-120">Vault/HSM Name : testmhsm Name           : testkey002 Version        : Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey002 Enabled        : False Expires        : 10/14/2022 8:13:29 AM Not Before     : 10/14/2020 8:13:33 AM Created        : 10/14/2020 8:14:01 AM Updated        : 10/14/2020 8:14:01 AM Recovery Level : Recoverable+Purgeable Tags           : Name        Value Severity    high Accounting  true</span></span>

<span data-ttu-id="a1990-121">Det här kommandot får alla nycklar i den hanterade HSM som heter testmhsm.</span><span class="sxs-lookup"><span data-stu-id="a1990-121">This command gets all the keys in the managed HSM named testmhsm.</span></span>

### <span data-ttu-id="a1990-122">Exempel 2: hämta den aktuella versionen av en-tangenten</span><span class="sxs-lookup"><span data-stu-id="a1990-122">Example 2: Get the current version of a key</span></span>
```powershell
PS C:\>$hsm = Get-AzManagedHsmKey -HsmName testmhsm -KeyName testkey001
PS C:\>$hsm

Vault/HSM Name : testmhsm
Name           : testkey001
Version        : 9a9de2bcec540c3b160cd54cbae71339
Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey/9a9de2bcec540c3b160cd54cbae71339
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

<span data-ttu-id="a1990-123">Med det här kommandot får du den aktuella versionen av den Key som heter testkey001 i den hanterade HSM som heter testmhsm.</span><span class="sxs-lookup"><span data-stu-id="a1990-123">This command gets the current version of the key named testkey001 in the managed HSM named testmhsm.</span></span>
<span data-ttu-id="a1990-124">Obs! HSM-namnet kan erhållas genom $hsm. VaultName</span><span class="sxs-lookup"><span data-stu-id="a1990-124">Note: Hsm Name can be obtained by $hsm.VaultName</span></span>

### <span data-ttu-id="a1990-125">Exempel 3: Hämta alla versioner av en viktig</span><span class="sxs-lookup"><span data-stu-id="a1990-125">Example 3: Get all versions of a key</span></span>
```powershell
PS C:\> Get-AzManagedHsmKey -HsmName testmhsm -KeyName testkey001 -IncludeVersions

Vault/HSM Name : testmhsm
Name           : testkey001
Version        : 80fd43e31e8649873520053c91148418
Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey001/80fd43e31e8649873520053c91148418
Enabled        : True
Expires        :
Not Before     :
Created        : 10/14/2020 8:06:26 AM
Updated        : 10/14/2020 8:06:26 AM
Recovery Level : Recoverable+Purgeable
Tags           :

Vault/HSM Name : testmhsm
Name           : testkey001
Version        : 9a9de2bcec540c3b160cd54cbae71339
Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey001/9a9de2bcec540c3b160cd54cbae71339
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

<span data-ttu-id="a1990-126">Med det här kommandot får alla versioner den nycklar som heter testkey001 i den hanterade HSM som heter testmhsm.</span><span class="sxs-lookup"><span data-stu-id="a1990-126">This command gets all versions the key named testkey001 in the managed HSM named testmhsm.</span></span>

### <span data-ttu-id="a1990-127">Exempel 4: skaffa en specifik version av en</span><span class="sxs-lookup"><span data-stu-id="a1990-127">Example 4: Get a specific version of a key</span></span>
```powershell
PS C:\> Get-AzManagedHsmKey -HsmName testmhsm -KeyName testkey -Version 80fd43e31e8649873520053c91148418

Vault/HSM Name : testmhsm
Name           : testkey
Version        : 80fd43e31e8649873520053c91148418
Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey/80fd43e31e8649873520053c91148418
Enabled        : True
Expires        :
Not Before     :
Created        : 10/14/2020 8:06:26 AM
Updated        : 10/14/2020 8:06:26 AM
Recovery Level : Recoverable+Purgeable
Tags           :
```

<span data-ttu-id="a1990-128">Det här kommandot får en specifik version av den nycklar som heter testkey i den hanterade HSM som heter testmhsm.</span><span class="sxs-lookup"><span data-stu-id="a1990-128">This command gets a specific version of the key named testkey in the managed HSM named testmhsm.</span></span>
<span data-ttu-id="a1990-129">När du har kört det här kommandot kan du kontrol lera olika egenskaper för tangenten genom att navigera $Key-objektet.</span><span class="sxs-lookup"><span data-stu-id="a1990-129">After running this command, you can inspect various properties of the key by navigating the $Key object.</span></span>

### <span data-ttu-id="a1990-130">Exempel 5: Hämta alla nycklar som har tagits bort men inte rensats för den här hanterade HSM</span><span class="sxs-lookup"><span data-stu-id="a1990-130">Example 5: Get all the keys that have been deleted but not purged for this managed HSM</span></span>
```powershell
PS C:\> Get-AzManagedHsmKey -HsmName testmhsm -InRemovedState

Vault/HSM Name       : testmhsm
Name                 : testkey
Id                   : https://testmhsm.managedhsm.azure.net:443/keys/testkey
Deleted Date         : 10/14/2020 9:10:42 AM
Scheduled Purge Date : 1/12/2021 9:10:42 AM
Enabled              : False
Expires              : 10/14/2022 8:13:29 AM
Not Before           : 10/14/2020 8:13:33 AM
Created              : 10/14/2020 8:14:01 AM
Updated              : 10/14/2020 8:14:01 AM
Recovery Level       : Recoverable+Purgeable
Tags                 : Name        Value
                       Severity    high
                       Accounting  true                :
```

<span data-ttu-id="a1990-131">Det här kommandot får alla de nycklar som tidigare tagits bort, men inte rensats, i den hanterade HSM med namnet testmhsm.</span><span class="sxs-lookup"><span data-stu-id="a1990-131">This command gets all the keys that have been previously deleted, but not purged, in the managed HSM named testmhsm.</span></span>

### <span data-ttu-id="a1990-132">Exempel 6: hämtar det testkey som har tagits bort men inte rensats för denna hanterade HSM</span><span class="sxs-lookup"><span data-stu-id="a1990-132">Example 6: Gets the key testkey that has been deleted but not purged for this managed HSM</span></span>
```powershell
PS C:\>  Get-AzManagedHsmKey -HsmName testmhsm -Name testkey -InRemovedState 

Vault/HSM Name       : testmhsm
Name                 : testkey
Id                   : https://testmhsm.managedhsm.azure.net:443/keys/testkey/9a9de2bcec540c3b160cd54cbae71339
Deleted Date         : 10/14/2020 9:10:42 AM
Scheduled Purge Date : 1/12/2021 9:10:42 AM
Enabled              : False
Expires              : 10/14/2022 8:13:29 AM
Not Before           : 10/14/2020 8:13:33 AM
Created              : 10/14/2020 8:14:01 AM
Updated              : 10/14/2020 8:14:01 AM
Recovery Level       : Recoverable+Purgeable
Tags                 :
```

<span data-ttu-id="a1990-133">Det här kommandot får den testkey som du har tagit bort tidigare, men inte rensat, i den hanterade HSM med namnet testmhsm.</span><span class="sxs-lookup"><span data-stu-id="a1990-133">This command gets the key testkey that has been previously deleted, but not purged, in the managed HSM named testmhsm.</span></span>
<span data-ttu-id="a1990-134">Det här kommandot returnerar metadata som borttagnings datum och det schemalagda rensnings datumet för den här borttagna tangenten.</span><span class="sxs-lookup"><span data-stu-id="a1990-134">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted key.</span></span>

### <span data-ttu-id="a1990-135">Exempel 7: Hämta alla nycklar i en hanterad HSM med hjälp av filtrering</span><span class="sxs-lookup"><span data-stu-id="a1990-135">Example 7: Get all the keys in a managed HSM using filtering</span></span>
```powershell
PS C:\> Get-AzManagedHsmKey -HsmName testmhsm -KeyName "test*"

Vault/HSM Name : testmhsm
Name           : testkey
Version        :
Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey
Enabled        : False
Expires        : 10/14/2022 8:13:29 AM
Not Before     : 10/14/2020 8:13:33 AM
Created        : 10/14/2020 8:14:01 AM
Updated        : 10/14/2020 8:14:01 AM
Recovery Level : Recoverable+Purgeable
Tags           :
```

<span data-ttu-id="a1990-136">Det här kommandot får alla nycklar i den hanterade HSM med namnet testmhsm som börjar med "test".</span><span class="sxs-lookup"><span data-stu-id="a1990-136">This command gets all the keys in the managed HSM named testmhsm that start with "test".</span></span>

### <span data-ttu-id="a1990-137">Exempel 8: Ladda ned en offentlig fil som en. PEM-fil</span><span class="sxs-lookup"><span data-stu-id="a1990-137">Example 8: Download a public key as a .pem file</span></span>

```powershell
PS C:\> Get-AzManagedHsmKey -HsmName bezmhsm -Name testkey -OutFile  "C:\public.pem"

Vault/HSM Name : testmhsm
Name           : testkey
Version        :
Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey
Enabled        : False
Expires        : 10/14/2022 8:13:29 AM
Not Before     : 10/14/2020 8:13:33 AM
Created        : 10/14/2020 8:14:01 AM
Updated        : 10/14/2020 8:14:01 AM
Recovery Level : Recoverable+Purgeable
Tags           :
```

<span data-ttu-id="a1990-138">Du kan ladda ned den offentliga knappen för en RSA-fil genom att ange `-OutFile` parametern.</span><span class="sxs-lookup"><span data-stu-id="a1990-138">You can download the public key of a RSA key by specifying the `-OutFile` parameter.</span></span>

## <span data-ttu-id="a1990-139">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a1990-139">PARAMETERS</span></span>

### <span data-ttu-id="a1990-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1990-140">-DefaultProfile</span></span>
<span data-ttu-id="a1990-141">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a1990-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1990-142">-HsmName</span><span class="sxs-lookup"><span data-stu-id="a1990-142">-HsmName</span></span>
<span data-ttu-id="a1990-143">HSM-namn.</span><span class="sxs-lookup"><span data-stu-id="a1990-143">HSM name.</span></span> <span data-ttu-id="a1990-144">Cmdlet konstruerar FQDN för en hanterad HSM baserat på namnet och den valda miljön.</span><span class="sxs-lookup"><span data-stu-id="a1990-144">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: SpecifyHsmByHsmNameGetKeyWithoutConstraint, SpecifyHsmByHsmNameGetKeyWithSpecifiedVersion, SpecifyHsmByHsmNameGetKeyIncludeAllVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1990-145">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="a1990-145">-IncludeVersions</span></span>
<span data-ttu-id="a1990-146">Anger om de olika versionerna av nycklarna ska tas med i resultatet.</span><span class="sxs-lookup"><span data-stu-id="a1990-146">Specifies whether to include the versions of the key in the output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SpecifyHsmByHsmNameGetKeyIncludeAllVersions, SpecifyHsmByInputObjectGetKeyIncludeAllVersions, SpecifyHsmByResourceIdGetKeyIncludeAllVersions
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1990-147">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a1990-147">-InputObject</span></span>
<span data-ttu-id="a1990-148">HSM-objekt.</span><span class="sxs-lookup"><span data-stu-id="a1990-148">HSM object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: SpecifyHsmByInputObjectGetKeyWithoutConstraint, SpecifyHsmByInputObjectGetKeyWithSpecifiedVersion, SpecifyHsmByInputObjectGetKeyIncludeAllVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a1990-149">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="a1990-149">-InRemovedState</span></span>
<span data-ttu-id="a1990-150">Anger om tidigare borttagna nycklar ska visas i resultatet.</span><span class="sxs-lookup"><span data-stu-id="a1990-150">Specifies whether to show the previously deleted keys in the output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SpecifyHsmByHsmNameGetKeyWithoutConstraint, SpecifyHsmByInputObjectGetKeyWithoutConstraint, SpecifyHsmByResourceIdGetKeyWithoutConstraint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1990-151">-Namn</span><span class="sxs-lookup"><span data-stu-id="a1990-151">-Name</span></span>
<span data-ttu-id="a1990-152">Namn på knappen.</span><span class="sxs-lookup"><span data-stu-id="a1990-152">Key name.</span></span>
<span data-ttu-id="a1990-153">Cmdlet konstruerar FQDN för en Key från Managed HSM-namn, markerat miljö-och namn för tillfället.</span><span class="sxs-lookup"><span data-stu-id="a1990-153">Cmdlet constructs the FQDN of a key from managed HSM name, currently selected environment and key name.</span></span>

```yaml
Type: System.String
Parameter Sets: SpecifyHsmByHsmNameGetKeyWithoutConstraint, SpecifyHsmByInputObjectGetKeyWithoutConstraint, SpecifyHsmByResourceIdGetKeyWithoutConstraint
Aliases: KeyName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SpecifyHsmByHsmNameGetKeyWithSpecifiedVersion, SpecifyHsmByHsmNameGetKeyIncludeAllVersions, SpecifyHsmByInputObjectGetKeyWithSpecifiedVersion, SpecifyHsmByInputObjectGetKeyIncludeAllVersions, SpecifyHsmByResourceIdGetKeyWithSpecifiedVersion, SpecifyHsmByResourceIdGetKeyIncludeAllVersions
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1990-154">-Utdatafil</span><span class="sxs-lookup"><span data-stu-id="a1990-154">-OutFile</span></span>
<span data-ttu-id="a1990-155">Anger den utdatafil som den här cmdleten sparar för.</span><span class="sxs-lookup"><span data-stu-id="a1990-155">Specifies the output file for which this cmdlet saves the key.</span></span>
<span data-ttu-id="a1990-156">Den offentliga knappen sparas som standard i PEM-format.</span><span class="sxs-lookup"><span data-stu-id="a1990-156">The public key is saved in PEM format by default.</span></span>

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

### <span data-ttu-id="a1990-157">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a1990-157">-ResourceId</span></span>
<span data-ttu-id="a1990-158">HSM-resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="a1990-158">HSM Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: SpecifyHsmByResourceIdGetKeyWithoutConstraint, SpecifyHsmByResourceIdGetKeyWithSpecifiedVersion, SpecifyHsmByResourceIdGetKeyIncludeAllVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1990-159">-Version</span><span class="sxs-lookup"><span data-stu-id="a1990-159">-Version</span></span>
<span data-ttu-id="a1990-160">Huvud version.</span><span class="sxs-lookup"><span data-stu-id="a1990-160">Key version.</span></span>
<span data-ttu-id="a1990-161">Cmdlet konstruerar FQDN för en Key från Managed HSM-namn, markerad miljö, namn och viktig version.</span><span class="sxs-lookup"><span data-stu-id="a1990-161">Cmdlet constructs the FQDN of a key from managed HSM name, currently selected environment, key name and key version.</span></span>

```yaml
Type: System.String
Parameter Sets: SpecifyHsmByHsmNameGetKeyWithSpecifiedVersion, SpecifyHsmByInputObjectGetKeyWithSpecifiedVersion, SpecifyHsmByResourceIdGetKeyWithSpecifiedVersion
Aliases: KeyVersion

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1990-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1990-162">CommonParameters</span></span>
<span data-ttu-id="a1990-163">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1990-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1990-164">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a1990-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1990-165">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a1990-165">INPUTS</span></span>

### <span data-ttu-id="a1990-166">Microsoft. Azure. commands. valv. Models. PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="a1990-166">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="a1990-167">System. String</span><span class="sxs-lookup"><span data-stu-id="a1990-167">System.String</span></span>

## <span data-ttu-id="a1990-168">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a1990-168">OUTPUTS</span></span>

### <span data-ttu-id="a1990-169">Microsoft. Azure. commands. valv. Models. PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="a1990-169">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="a1990-170">Microsoft. Azure. commands. valv. Models. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="a1990-170">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

### <span data-ttu-id="a1990-171">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="a1990-171">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="a1990-172">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="a1990-172">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span></span>

## <span data-ttu-id="a1990-173">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a1990-173">NOTES</span></span>

## <span data-ttu-id="a1990-174">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a1990-174">RELATED LINKS</span></span>

[<span data-ttu-id="a1990-175">Add-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="a1990-175">Add-AzManagedHsmKey</span></span>](./Add-AzManagedHsmKey.md)

[<span data-ttu-id="a1990-176">Säkerhets kopiering-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="a1990-176">Backup-AzManagedHsmKey</span></span>](./Backup-AzManagedHsmKey.md)

[<span data-ttu-id="a1990-177">Remove-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="a1990-177">Remove-AzManagedHsmKey</span></span>](./Remove-AzManagedHsmKey.md)

[<span data-ttu-id="a1990-178">Ångra-AzManagedHsmKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="a1990-178">Undo-AzManagedHsmKeyRemoval</span></span>](./Undo-AzManagedHsmKeyRemoval.md)

[<span data-ttu-id="a1990-179">Update-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="a1990-179">Update-AzManagedHsmKey</span></span>](./Update-AzManagedHsmKey.md)

[<span data-ttu-id="a1990-180">Återställ-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="a1990-180">Restore-AzManagedHsmKey</span></span>](./Restore-AzManagedHsmKey.md)