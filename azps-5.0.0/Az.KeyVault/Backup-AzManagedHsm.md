---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzManagedHsm.md
ms.openlocfilehash: 5353adade342b7f73cf60ff6b0befa88f4a3da73
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94263046"
---
# <span data-ttu-id="9f319-101">Backup-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="9f319-101">Backup-AzManagedHsm</span></span>

## <span data-ttu-id="9f319-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9f319-102">SYNOPSIS</span></span>
<span data-ttu-id="9f319-103">Fullständig säkerhets kopiering av hanterad HSM.</span><span class="sxs-lookup"><span data-stu-id="9f319-103">Fully backup a managed HSM.</span></span>

## <span data-ttu-id="9f319-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9f319-104">SYNTAX</span></span>

### <span data-ttu-id="9f319-105">InteractiveStorageName (standard)</span><span class="sxs-lookup"><span data-stu-id="9f319-105">InteractiveStorageName (Default)</span></span>
```
Backup-AzManagedHsm [-Name] <String> -StorageAccountName <String> -StorageContainerName <String>
 -SasToken <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f319-106">InteractiveStorageUri</span><span class="sxs-lookup"><span data-stu-id="9f319-106">InteractiveStorageUri</span></span>
```
Backup-AzManagedHsm [-Name] <String> -StorageContainerUri <Uri> -SasToken <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f319-107">InputObjectStorageUri</span><span class="sxs-lookup"><span data-stu-id="9f319-107">InputObjectStorageUri</span></span>
```
Backup-AzManagedHsm -StorageContainerUri <Uri> -SasToken <SecureString> -HsmObject <PSManagedHsm>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f319-108">InputObjectStorageName</span><span class="sxs-lookup"><span data-stu-id="9f319-108">InputObjectStorageName</span></span>
```
Backup-AzManagedHsm -StorageAccountName <String> -StorageContainerName <String> -SasToken <SecureString>
 -HsmObject <PSManagedHsm> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f319-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9f319-109">DESCRIPTION</span></span>
<span data-ttu-id="9f319-110">Fullständig säkerhets kopiering av hanterad HSM till ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="9f319-110">Fully backup a managed HSM to a storage account.</span></span>
<span data-ttu-id="9f319-111">Använd detta `Restore-AzManagedHsm` för att återställa säkerhets kopian.</span><span class="sxs-lookup"><span data-stu-id="9f319-111">Use `Restore-AzManagedHsm` to restore the backup.</span></span>

## <span data-ttu-id="9f319-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9f319-112">EXAMPLES</span></span>

### <span data-ttu-id="9f319-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="9f319-113">Example 1</span></span>
```powershell
PS C:\> $sasToken = ConvertTo-SecureString -AsPlainText -Force "?sv=2019-12-12&ss=bfqt&srt=sco&sp=rwdlacupx&se=2020-10-12T14:42:19Z&st=2020-10-12T06:42:19Z&spr=https&sig=******"

PS C:\> Backup-AzManagedHsm -Name myHsm -StorageContainerUri "https://{accountName}.blob.core.windows.net/{containerName}" -SasToken $sasToken

https://{accountName}.blob.core.windows.net/{containerName}/{backupFolder}
```

<span data-ttu-id="9f319-114">Cmdleten skapar en mapp (vanligt vis namn `mhsm-{name}-{timestamp}` ) i lagrings behållaren, lagrar säkerhets kopian i den mappen och skriver ut mappen URI.</span><span class="sxs-lookup"><span data-stu-id="9f319-114">The cmdlet will create a folder (typically named `mhsm-{name}-{timestamp}`) in the storage container, store the backup in that folder and output the folder URI.</span></span>

## <span data-ttu-id="9f319-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9f319-115">PARAMETERS</span></span>

### <span data-ttu-id="9f319-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f319-116">-DefaultProfile</span></span>
<span data-ttu-id="9f319-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9f319-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f319-118">-HsmObject</span><span class="sxs-lookup"><span data-stu-id="9f319-118">-HsmObject</span></span>
<span data-ttu-id="9f319-119">Hanterat HSM-objekt</span><span class="sxs-lookup"><span data-stu-id="9f319-119">Managed HSM object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: InputObjectStorageUri, InputObjectStorageName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f319-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="9f319-120">-Name</span></span>
<span data-ttu-id="9f319-121">Namn på HSM.</span><span class="sxs-lookup"><span data-stu-id="9f319-121">Name of the HSM.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveStorageName, InteractiveStorageUri
Aliases: HsmName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f319-122">-SasToken</span><span class="sxs-lookup"><span data-stu-id="9f319-122">-SasToken</span></span>
<span data-ttu-id="9f319-123">Den delade Access-signaturen (SAS) för att autentisera lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="9f319-123">The shared access signature (SAS) token to authenticate the storage account.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f319-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="9f319-124">-StorageAccountName</span></span>
<span data-ttu-id="9f319-125">Namn på det lagrings konto där säkerhets kopian ska lagras.</span><span class="sxs-lookup"><span data-stu-id="9f319-125">Name of the storage account where the backup is going to be stored.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveStorageName, InputObjectStorageName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f319-126">-StorageContainerName</span><span class="sxs-lookup"><span data-stu-id="9f319-126">-StorageContainerName</span></span>
<span data-ttu-id="9f319-127">Namnet på BLOB-behållaren där säkerhets kopian ska lagras.</span><span class="sxs-lookup"><span data-stu-id="9f319-127">Name of the blob container where the backup is going to be stored.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveStorageName, InputObjectStorageName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f319-128">-StorageContainerUri</span><span class="sxs-lookup"><span data-stu-id="9f319-128">-StorageContainerUri</span></span>
<span data-ttu-id="9f319-129">URI för lagrings behållaren där säkerhets kopian ska lagras.</span><span class="sxs-lookup"><span data-stu-id="9f319-129">URI of the storage container where the backup is going to be stored.</span></span>

```yaml
Type: System.Uri
Parameter Sets: InteractiveStorageUri, InputObjectStorageUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f319-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9f319-130">-Confirm</span></span>
<span data-ttu-id="9f319-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9f319-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f319-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f319-132">-WhatIf</span></span>
<span data-ttu-id="9f319-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9f319-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f319-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9f319-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f319-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f319-135">CommonParameters</span></span>
<span data-ttu-id="9f319-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f319-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f319-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9f319-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f319-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9f319-138">INPUTS</span></span>

### <span data-ttu-id="9f319-139">Ingen</span><span class="sxs-lookup"><span data-stu-id="9f319-139">None</span></span>

## <span data-ttu-id="9f319-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9f319-140">OUTPUTS</span></span>

### <span data-ttu-id="9f319-141">System. String</span><span class="sxs-lookup"><span data-stu-id="9f319-141">System.String</span></span>

## <span data-ttu-id="9f319-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9f319-142">NOTES</span></span>

## <span data-ttu-id="9f319-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9f319-143">RELATED LINKS</span></span>
