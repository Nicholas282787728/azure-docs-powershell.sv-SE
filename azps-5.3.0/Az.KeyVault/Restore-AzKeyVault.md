---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/restore-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVault.md
ms.openlocfilehash: d1cf3757596a56336c25c46bd6c4e38687888d6e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98522595"
---
# <span data-ttu-id="1adad-101">Restore-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="1adad-101">Restore-AzKeyVault</span></span>

## <span data-ttu-id="1adad-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1adad-102">SYNOPSIS</span></span>
<span data-ttu-id="1adad-103">En hanterad HSM återställs helt från säkerhets kopian.</span><span class="sxs-lookup"><span data-stu-id="1adad-103">Fully restores a managed HSM from backup.</span></span>

## <span data-ttu-id="1adad-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1adad-104">SYNTAX</span></span>

### <span data-ttu-id="1adad-105">InteractiveStorageName (standard)</span><span class="sxs-lookup"><span data-stu-id="1adad-105">InteractiveStorageName (Default)</span></span>
```
Restore-AzKeyVault -BackupFolder <String> [-KeyName <String>] [-PassThru] [-HsmName] <String>
 -StorageAccountName <String> -StorageContainerName <String> -SasToken <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1adad-106">InteractiveStorageUri</span><span class="sxs-lookup"><span data-stu-id="1adad-106">InteractiveStorageUri</span></span>
```
Restore-AzKeyVault -BackupFolder <String> [-KeyName <String>] [-PassThru] [-HsmName] <String>
 -StorageContainerUri <Uri> -SasToken <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1adad-107">InputObjectStorageUri</span><span class="sxs-lookup"><span data-stu-id="1adad-107">InputObjectStorageUri</span></span>
```
Restore-AzKeyVault -BackupFolder <String> [-KeyName <String>] [-PassThru] -StorageContainerUri <Uri>
 -SasToken <SecureString> -HsmObject <PSManagedHsm> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1adad-108">InputObjectStorageName</span><span class="sxs-lookup"><span data-stu-id="1adad-108">InputObjectStorageName</span></span>
```
Restore-AzKeyVault -BackupFolder <String> [-KeyName <String>] [-PassThru] -StorageAccountName <String>
 -StorageContainerName <String> -SasToken <SecureString> -HsmObject <PSManagedHsm>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1adad-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1adad-109">DESCRIPTION</span></span>
<span data-ttu-id="1adad-110">Återställer en hanterad HSM fullständigt från en säkerhets kopia som lagras i ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="1adad-110">Fully restores a managed HSM from a backup stored in a storage account.</span></span>
<span data-ttu-id="1adad-111">Använd `Backup-AzKeyVault` för att säkerhetskopiera.</span><span class="sxs-lookup"><span data-stu-id="1adad-111">Use `Backup-AzKeyVault` to backup.</span></span>

## <span data-ttu-id="1adad-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1adad-112">EXAMPLES</span></span>

### <span data-ttu-id="1adad-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="1adad-113">Example 1</span></span>
```powershell
PS C:\> $sasToken = ConvertTo-SecureString -AsPlainText -Force "?sv=2019-12-12&ss=bfqt&srt=sco&sp=rwdlacupx&se=2020-10-12T14:42:19Z&st=2020-10-12T06:42:19Z&spr=https&sig=******"
PS C:\> Restore-AzKeyVault -HsmName myHsm -StorageContainerUri "https://{accountName}.blob.core.windows.net/{containerName}" -BackupFolder "mhsm-myHsm-2020101308504935" -SasToken $sasToken
```

<span data-ttu-id="1adad-114">Exemplet återställer en säkerhets kopia som är lagrad i en mapp med namnet "mhsm-myHsm-2020101308504935" i en lagrings behållare (https://{accountName}. blob. Core. Windows. net/{containerName} ".</span><span class="sxs-lookup"><span data-stu-id="1adad-114">The example restores a backup stored in a folder named "mhsm-myHsm-2020101308504935" of a storage container "https://{accountName}.blob.core.windows.net/{containerName}".</span></span>

## <span data-ttu-id="1adad-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1adad-115">PARAMETERS</span></span>

### <span data-ttu-id="1adad-116">-BackupFolder</span><span class="sxs-lookup"><span data-stu-id="1adad-116">-BackupFolder</span></span>
<span data-ttu-id="1adad-117">Namn på säkerhets kopian, till exempel "mhsm-*-2020101309020403". Det kan också vara kapslat som "säkerhets kopior/mhsm-*-2020101309020403".</span><span class="sxs-lookup"><span data-stu-id="1adad-117">Folder name of the backup, e.g. 'mhsm-*-2020101309020403'. It can also be nested such as 'backups/mhsm-*-2020101309020403'.</span></span>

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

### <span data-ttu-id="1adad-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1adad-118">-DefaultProfile</span></span>
<span data-ttu-id="1adad-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1adad-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1adad-120">-HsmName</span><span class="sxs-lookup"><span data-stu-id="1adad-120">-HsmName</span></span>
<span data-ttu-id="1adad-121">Namn på HSM.</span><span class="sxs-lookup"><span data-stu-id="1adad-121">Name of the HSM.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveStorageName, InteractiveStorageUri
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1adad-122">-HsmObject</span><span class="sxs-lookup"><span data-stu-id="1adad-122">-HsmObject</span></span>
<span data-ttu-id="1adad-123">Hanterat HSM-objekt</span><span class="sxs-lookup"><span data-stu-id="1adad-123">Managed HSM object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: InputObjectStorageUri, InputObjectStorageName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1adad-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="1adad-124">-KeyName</span></span>
<span data-ttu-id="1adad-125">Namn som ska återställas.</span><span class="sxs-lookup"><span data-stu-id="1adad-125">Key name to restore.</span></span>

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

### <span data-ttu-id="1adad-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1adad-126">-PassThru</span></span>
<span data-ttu-id="1adad-127">Returnera true när HSM återställs.</span><span class="sxs-lookup"><span data-stu-id="1adad-127">Return true when the HSM is restored.</span></span>

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

### <span data-ttu-id="1adad-128">-SasToken</span><span class="sxs-lookup"><span data-stu-id="1adad-128">-SasToken</span></span>
<span data-ttu-id="1adad-129">Den delade Access-signaturen (SAS) för att autentisera lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="1adad-129">The shared access signature (SAS) token to authenticate the storage account.</span></span>

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

### <span data-ttu-id="1adad-130">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="1adad-130">-StorageAccountName</span></span>
<span data-ttu-id="1adad-131">Namn på det lagrings konto där säkerhets kopian ska lagras.</span><span class="sxs-lookup"><span data-stu-id="1adad-131">Name of the storage account where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="1adad-132">-StorageContainerName</span><span class="sxs-lookup"><span data-stu-id="1adad-132">-StorageContainerName</span></span>
<span data-ttu-id="1adad-133">Namnet på BLOB-behållaren där säkerhets kopian ska lagras.</span><span class="sxs-lookup"><span data-stu-id="1adad-133">Name of the blob container where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="1adad-134">-StorageContainerUri</span><span class="sxs-lookup"><span data-stu-id="1adad-134">-StorageContainerUri</span></span>
<span data-ttu-id="1adad-135">URI för lagrings behållaren där säkerhets kopian ska lagras.</span><span class="sxs-lookup"><span data-stu-id="1adad-135">URI of the storage container where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="1adad-136">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1adad-136">-Confirm</span></span>
<span data-ttu-id="1adad-137">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1adad-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1adad-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1adad-138">-WhatIf</span></span>
<span data-ttu-id="1adad-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1adad-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1adad-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1adad-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1adad-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1adad-141">CommonParameters</span></span>
<span data-ttu-id="1adad-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1adad-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1adad-143">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1adad-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1adad-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1adad-144">INPUTS</span></span>

### <span data-ttu-id="1adad-145">Ingen</span><span class="sxs-lookup"><span data-stu-id="1adad-145">None</span></span>

## <span data-ttu-id="1adad-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1adad-146">OUTPUTS</span></span>

### <span data-ttu-id="1adad-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1adad-147">System.Boolean</span></span>

## <span data-ttu-id="1adad-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1adad-148">NOTES</span></span>

## <span data-ttu-id="1adad-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1adad-149">RELATED LINKS</span></span>
