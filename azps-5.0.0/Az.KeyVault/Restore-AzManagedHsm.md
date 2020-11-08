---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/restore-azmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzManagedHsm.md
ms.openlocfilehash: 97e5c836d7d6b209d31851264047c6df894d77a7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94273436"
---
# <span data-ttu-id="48854-101">Restore-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="48854-101">Restore-AzManagedHsm</span></span>

## <span data-ttu-id="48854-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="48854-102">SYNOPSIS</span></span>
<span data-ttu-id="48854-103">En hanterad HSM återställs helt från säkerhets kopian.</span><span class="sxs-lookup"><span data-stu-id="48854-103">Fully restores a managed HSM from backup.</span></span>

## <span data-ttu-id="48854-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="48854-104">SYNTAX</span></span>

### <span data-ttu-id="48854-105">InteractiveStorageName (standard)</span><span class="sxs-lookup"><span data-stu-id="48854-105">InteractiveStorageName (Default)</span></span>
```
Restore-AzManagedHsm -BackupFolder <String> [-PassThru] [-Name] <String> -StorageAccountName <String>
 -StorageContainerName <String> -SasToken <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48854-106">InteractiveStorageUri</span><span class="sxs-lookup"><span data-stu-id="48854-106">InteractiveStorageUri</span></span>
```
Restore-AzManagedHsm -BackupFolder <String> [-PassThru] [-Name] <String> -StorageContainerUri <Uri>
 -SasToken <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48854-107">InputObjectStorageUri</span><span class="sxs-lookup"><span data-stu-id="48854-107">InputObjectStorageUri</span></span>
```
Restore-AzManagedHsm -BackupFolder <String> [-PassThru] -StorageContainerUri <Uri> -SasToken <SecureString>
 -HsmObject <PSManagedHsm> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48854-108">InputObjectStorageName</span><span class="sxs-lookup"><span data-stu-id="48854-108">InputObjectStorageName</span></span>
```
Restore-AzManagedHsm -BackupFolder <String> [-PassThru] -StorageAccountName <String>
 -StorageContainerName <String> -SasToken <SecureString> -HsmObject <PSManagedHsm>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48854-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="48854-109">DESCRIPTION</span></span>
<span data-ttu-id="48854-110">Återställer en hanterad HSM fullständigt från en säkerhets kopia som lagras i ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="48854-110">Fully restores a managed HSM from a backup stored in a storage account.</span></span>
<span data-ttu-id="48854-111">Använd `Backup-AzManagedHsm` för att säkerhetskopiera.</span><span class="sxs-lookup"><span data-stu-id="48854-111">Use `Backup-AzManagedHsm` to backup.</span></span>

## <span data-ttu-id="48854-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="48854-112">EXAMPLES</span></span>

### <span data-ttu-id="48854-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="48854-113">Example 1</span></span>
```powershell
PS C:\> $sasToken = ConvertTo-SecureString -AsPlainText -Force "?sv=2019-12-12&ss=bfqt&srt=sco&sp=rwdlacupx&se=2020-10-12T14:42:19Z&st=2020-10-12T06:42:19Z&spr=https&sig=******"
PS C:\> Restore-AzManagedHsm -Name myHsm -StorageContainerUri "https://{accountName}.blob.core.windows.net/{containerName}" -BackupFolder "mhsm-myHsm-2020101308504935" -SasToken $sasToken
```

<span data-ttu-id="48854-114">Exemplet återställer en säkerhets kopia som är lagrad i en mapp med namnet "mhsm-myHsm-2020101308504935" i en lagrings behållare (https://{accountName}. blob. Core. Windows. net/{containerName} ".</span><span class="sxs-lookup"><span data-stu-id="48854-114">The example restores a backup stored in a folder named "mhsm-myHsm-2020101308504935" of a storage container "https://{accountName}.blob.core.windows.net/{containerName}".</span></span>

## <span data-ttu-id="48854-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="48854-115">PARAMETERS</span></span>

### <span data-ttu-id="48854-116">-BackupFolder</span><span class="sxs-lookup"><span data-stu-id="48854-116">-BackupFolder</span></span>
<span data-ttu-id="48854-117">Namn på säkerhets kopian, till exempel "mhsm- *-2020101309020403". Det kan också vara kapslat som "säkerhets kopior/mhsm-* -2020101309020403".</span><span class="sxs-lookup"><span data-stu-id="48854-117">Folder name of the backup, e.g. 'mhsm- *-2020101309020403'. It can also be nested such as 'backups/mhsm-* -2020101309020403'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48854-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48854-118">-DefaultProfile</span></span>
<span data-ttu-id="48854-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="48854-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48854-120">-HsmObject</span><span class="sxs-lookup"><span data-stu-id="48854-120">-HsmObject</span></span>
<span data-ttu-id="48854-121">Hanterat HSM-objekt</span><span class="sxs-lookup"><span data-stu-id="48854-121">Managed HSM object</span></span>

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

### <span data-ttu-id="48854-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="48854-122">-Name</span></span>
<span data-ttu-id="48854-123">Namn på HSM.</span><span class="sxs-lookup"><span data-stu-id="48854-123">Name of the HSM.</span></span>

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

### <span data-ttu-id="48854-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="48854-124">-PassThru</span></span>
<span data-ttu-id="48854-125">Returnera true när HSM återställs.</span><span class="sxs-lookup"><span data-stu-id="48854-125">Return true when the HSM is restored.</span></span>

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

### <span data-ttu-id="48854-126">-SasToken</span><span class="sxs-lookup"><span data-stu-id="48854-126">-SasToken</span></span>
<span data-ttu-id="48854-127">Den delade Access-signaturen (SAS) för att autentisera lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="48854-127">The shared access signature (SAS) token to authenticate the storage account.</span></span>

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

### <span data-ttu-id="48854-128">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="48854-128">-StorageAccountName</span></span>
<span data-ttu-id="48854-129">Namn på det lagrings konto där säkerhets kopian ska lagras.</span><span class="sxs-lookup"><span data-stu-id="48854-129">Name of the storage account where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="48854-130">-StorageContainerName</span><span class="sxs-lookup"><span data-stu-id="48854-130">-StorageContainerName</span></span>
<span data-ttu-id="48854-131">Namnet på BLOB-behållaren där säkerhets kopian ska lagras.</span><span class="sxs-lookup"><span data-stu-id="48854-131">Name of the blob container where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="48854-132">-StorageContainerUri</span><span class="sxs-lookup"><span data-stu-id="48854-132">-StorageContainerUri</span></span>
<span data-ttu-id="48854-133">URI för lagrings behållaren där säkerhets kopian ska lagras.</span><span class="sxs-lookup"><span data-stu-id="48854-133">URI of the storage container where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="48854-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="48854-134">-Confirm</span></span>
<span data-ttu-id="48854-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="48854-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48854-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48854-136">-WhatIf</span></span>
<span data-ttu-id="48854-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="48854-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48854-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="48854-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48854-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48854-139">CommonParameters</span></span>
<span data-ttu-id="48854-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48854-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48854-141">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="48854-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48854-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="48854-142">INPUTS</span></span>

### <span data-ttu-id="48854-143">Ingen</span><span class="sxs-lookup"><span data-stu-id="48854-143">None</span></span>

## <span data-ttu-id="48854-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="48854-144">OUTPUTS</span></span>

### <span data-ttu-id="48854-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="48854-145">System.Boolean</span></span>

## <span data-ttu-id="48854-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="48854-146">NOTES</span></span>

## <span data-ttu-id="48854-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="48854-147">RELATED LINKS</span></span>
