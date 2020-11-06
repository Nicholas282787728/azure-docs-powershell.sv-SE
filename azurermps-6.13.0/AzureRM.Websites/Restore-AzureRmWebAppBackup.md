---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: DC400E32-CAB9-4354-99B2-ABA4AA776030
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/restore-azurermwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restore-AzureRmWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restore-AzureRmWebAppBackup.md
ms.openlocfilehash: efb570c22b5345b9d75fdf96dca061dc5cf7847f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577728"
---
# <span data-ttu-id="e6d9b-101">Restore-AzureRmWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="e6d9b-101">Restore-AzureRmWebAppBackup</span></span>

## <span data-ttu-id="e6d9b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e6d9b-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e6d9b-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e6d9b-103">SYNTAX</span></span>

### <span data-ttu-id="e6d9b-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="e6d9b-104">FromResourceName</span></span>
```
Restore-AzureRmWebAppBackup [-AppServicePlan <String>] [-Databases <DatabaseBackupSetting[]>]
 [-IgnoreConflictingHostNames] [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String> [-BlobName] <String> [-Overwrite]
 [<CommonParameters>]
```

### <span data-ttu-id="e6d9b-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="e6d9b-105">FromWebApp</span></span>
```
Restore-AzureRmWebAppBackup [-AppServicePlan <String>] [-Databases <DatabaseBackupSetting[]>]
 [-IgnoreConflictingHostNames] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [-BlobName] <String> [-Overwrite] [<CommonParameters>]
```

## <span data-ttu-id="e6d9b-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e6d9b-106">DESCRIPTION</span></span>
<span data-ttu-id="e6d9b-107">Cmdleten **restore-AzureRmWebAppBackup** återställer en Azure Web App-säkerhetskopia.</span><span class="sxs-lookup"><span data-stu-id="e6d9b-107">The **Restore-AzureRmWebAppBackup** cmdlet restores an Azure Web App Backup.</span></span>

## <span data-ttu-id="e6d9b-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e6d9b-108">EXAMPLES</span></span>

### <span data-ttu-id="e6d9b-109">9.1</span><span class="sxs-lookup"><span data-stu-id="e6d9b-109">1:</span></span>
```
PS C:\> Restore-AzureRmWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StorageAccountUrl "https://storageaccount.file.core.windows.net" -BlobName "myBlob"
```

<span data-ttu-id="e6d9b-110">Återställer en säkerhets kopia av den angivna app-ContosoWebApp som ingår i resurs gruppens standardinställning-väst i BLOB "mittArkiv" på https://storageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="e6d9b-110">Restores a backup of the specified app ContosoWebApp that is within resource group Default-Web-WestUS in blob "myBlob" located at https://storageaccount.file.core.windows.net</span></span>

## <span data-ttu-id="e6d9b-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e6d9b-111">PARAMETERS</span></span>

### <span data-ttu-id="e6d9b-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="e6d9b-112">-AppServicePlan</span></span>
<span data-ttu-id="e6d9b-113">Namnet på App Service-planen för det återställda programmet.</span><span class="sxs-lookup"><span data-stu-id="e6d9b-113">The name of the App Service Plan for the restored app.</span></span> <span data-ttu-id="e6d9b-114">Om du lämnar det här alternativet används appens nuvarande App Service-plan.</span><span class="sxs-lookup"><span data-stu-id="e6d9b-114">If left empty, the app's current App Service Plan is used.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6d9b-115">-BlobName</span><span class="sxs-lookup"><span data-stu-id="e6d9b-115">-BlobName</span></span>
<span data-ttu-id="e6d9b-116">BLOB-namn</span><span class="sxs-lookup"><span data-stu-id="e6d9b-116">Blob Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6d9b-117">-Databaser</span><span class="sxs-lookup"><span data-stu-id="e6d9b-117">-Databases</span></span>
<span data-ttu-id="e6d9b-118">Databaser av typen DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="e6d9b-118">Databases of type DatabaseBackupSetting[]</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6d9b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6d9b-119">-DefaultProfile</span></span>
<span data-ttu-id="e6d9b-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e6d9b-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6d9b-121">-IgnoreConflictingHostNames</span><span class="sxs-lookup"><span data-stu-id="e6d9b-121">-IgnoreConflictingHostNames</span></span>
<span data-ttu-id="e6d9b-122">Ignorera alternativ för värdbaserade namn</span><span class="sxs-lookup"><span data-stu-id="e6d9b-122">Ignore Conflicting HostNames Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6d9b-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="e6d9b-123">-Name</span></span>
<span data-ttu-id="e6d9b-124">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="e6d9b-124">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6d9b-125">-Skriver över</span><span class="sxs-lookup"><span data-stu-id="e6d9b-125">-Overwrite</span></span>
<span data-ttu-id="e6d9b-126">Alternativet överskrivning</span><span class="sxs-lookup"><span data-stu-id="e6d9b-126">Overwrite Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6d9b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6d9b-127">-ResourceGroupName</span></span>
<span data-ttu-id="e6d9b-128">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="e6d9b-128">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6d9b-129">-Plats</span><span class="sxs-lookup"><span data-stu-id="e6d9b-129">-Slot</span></span>
<span data-ttu-id="e6d9b-130">WebApp-slot</span><span class="sxs-lookup"><span data-stu-id="e6d9b-130">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6d9b-131">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="e6d9b-131">-StorageAccountUrl</span></span>
<span data-ttu-id="e6d9b-132">URL för lagrings konto</span><span class="sxs-lookup"><span data-stu-id="e6d9b-132">Storage Account Url</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6d9b-133">-WebApp</span><span class="sxs-lookup"><span data-stu-id="e6d9b-133">-WebApp</span></span>
<span data-ttu-id="e6d9b-134">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="e6d9b-134">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: FromWebApp
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e6d9b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6d9b-135">CommonParameters</span></span>
<span data-ttu-id="e6d9b-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6d9b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6d9b-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6d9b-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6d9b-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e6d9b-138">INPUTS</span></span>

### <span data-ttu-id="e6d9b-139">System. String</span><span class="sxs-lookup"><span data-stu-id="e6d9b-139">System.String</span></span>

### <span data-ttu-id="e6d9b-140">Microsoft. Azure. Management. webbplatser. Models. DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="e6d9b-140">Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting[]</span></span>

### <span data-ttu-id="e6d9b-141">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e6d9b-141">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="e6d9b-142">Microsoft. Azure. Management. webbplatser. Models. site</span><span class="sxs-lookup"><span data-stu-id="e6d9b-142">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="e6d9b-143">Parametrar: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e6d9b-143">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="e6d9b-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e6d9b-144">OUTPUTS</span></span>

### <span data-ttu-id="e6d9b-145">System. Void</span><span class="sxs-lookup"><span data-stu-id="e6d9b-145">System.Void</span></span>

## <span data-ttu-id="e6d9b-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e6d9b-146">NOTES</span></span>

## <span data-ttu-id="e6d9b-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e6d9b-147">RELATED LINKS</span></span>
