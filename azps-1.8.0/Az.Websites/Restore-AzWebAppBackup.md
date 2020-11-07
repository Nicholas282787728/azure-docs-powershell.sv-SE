---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: DC400E32-CAB9-4354-99B2-ABA4AA776030
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/restore-azwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzWebAppBackup.md
ms.openlocfilehash: 94fbc71db34ca0abc6a27130dc166318794e271a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746029"
---
# <span data-ttu-id="fcc1c-101">Restore-AzWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="fcc1c-101">Restore-AzWebAppBackup</span></span>

## <span data-ttu-id="fcc1c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fcc1c-102">SYNOPSIS</span></span>

## <span data-ttu-id="fcc1c-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fcc1c-103">SYNTAX</span></span>

### <span data-ttu-id="fcc1c-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="fcc1c-104">FromResourceName</span></span>
```
Restore-AzWebAppBackup [-AppServicePlan <String>] [-Databases <DatabaseBackupSetting[]>]
 [-IgnoreConflictingHostNames] [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String> [-BlobName] <String> [-Overwrite]
 [<CommonParameters>]
```

### <span data-ttu-id="fcc1c-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="fcc1c-105">FromWebApp</span></span>
```
Restore-AzWebAppBackup [-AppServicePlan <String>] [-Databases <DatabaseBackupSetting[]>]
 [-IgnoreConflictingHostNames] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [-BlobName] <String> [-Overwrite] [<CommonParameters>]
```

## <span data-ttu-id="fcc1c-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fcc1c-106">DESCRIPTION</span></span>
<span data-ttu-id="fcc1c-107">Cmdleten **restore-AzWebAppBackup** återställer en Azure Web App-säkerhetskopia.</span><span class="sxs-lookup"><span data-stu-id="fcc1c-107">The **Restore-AzWebAppBackup** cmdlet restores an Azure Web App Backup.</span></span>

## <span data-ttu-id="fcc1c-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fcc1c-108">EXAMPLES</span></span>

### <span data-ttu-id="fcc1c-109">9.1</span><span class="sxs-lookup"><span data-stu-id="fcc1c-109">1:</span></span>
```
PS C:\> Restore-AzWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StorageAccountUrl "https://storageaccount.file.core.windows.net" -BlobName "myBlob"
```

<span data-ttu-id="fcc1c-110">Återställer en säkerhets kopia av den angivna app-ContosoWebApp som ingår i resurs gruppens standardinställning-väst i BLOB "mittArkiv" på https://storageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="fcc1c-110">Restores a backup of the specified app ContosoWebApp that is within resource group Default-Web-WestUS in blob "myBlob" located at https://storageaccount.file.core.windows.net</span></span>

## <span data-ttu-id="fcc1c-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fcc1c-111">PARAMETERS</span></span>

### <span data-ttu-id="fcc1c-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="fcc1c-112">-AppServicePlan</span></span>
<span data-ttu-id="fcc1c-113">Namnet på App Service-planen för det återställda programmet.</span><span class="sxs-lookup"><span data-stu-id="fcc1c-113">The name of the App Service Plan for the restored app.</span></span> <span data-ttu-id="fcc1c-114">Om du lämnar det här alternativet används appens nuvarande App Service-plan.</span><span class="sxs-lookup"><span data-stu-id="fcc1c-114">If left empty, the app's current App Service Plan is used.</span></span>

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

### <span data-ttu-id="fcc1c-115">-BlobName</span><span class="sxs-lookup"><span data-stu-id="fcc1c-115">-BlobName</span></span>
<span data-ttu-id="fcc1c-116">BLOB-namn</span><span class="sxs-lookup"><span data-stu-id="fcc1c-116">Blob Name</span></span>

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

### <span data-ttu-id="fcc1c-117">-Databaser</span><span class="sxs-lookup"><span data-stu-id="fcc1c-117">-Databases</span></span>
<span data-ttu-id="fcc1c-118">Databaser av typen DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="fcc1c-118">Databases of type DatabaseBackupSetting[]</span></span>

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

### <span data-ttu-id="fcc1c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcc1c-119">-DefaultProfile</span></span>
<span data-ttu-id="fcc1c-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fcc1c-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fcc1c-121">-IgnoreConflictingHostNames</span><span class="sxs-lookup"><span data-stu-id="fcc1c-121">-IgnoreConflictingHostNames</span></span>
<span data-ttu-id="fcc1c-122">Ignorera alternativ för värdbaserade namn</span><span class="sxs-lookup"><span data-stu-id="fcc1c-122">Ignore Conflicting HostNames Option</span></span>

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

### <span data-ttu-id="fcc1c-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="fcc1c-123">-Name</span></span>
<span data-ttu-id="fcc1c-124">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="fcc1c-124">WebApp Name</span></span>

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

### <span data-ttu-id="fcc1c-125">-Skriver över</span><span class="sxs-lookup"><span data-stu-id="fcc1c-125">-Overwrite</span></span>
<span data-ttu-id="fcc1c-126">Alternativet överskrivning</span><span class="sxs-lookup"><span data-stu-id="fcc1c-126">Overwrite Option</span></span>

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

### <span data-ttu-id="fcc1c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fcc1c-127">-ResourceGroupName</span></span>
<span data-ttu-id="fcc1c-128">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="fcc1c-128">Resource Group Name</span></span>

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

### <span data-ttu-id="fcc1c-129">-Plats</span><span class="sxs-lookup"><span data-stu-id="fcc1c-129">-Slot</span></span>
<span data-ttu-id="fcc1c-130">WebApp-slot</span><span class="sxs-lookup"><span data-stu-id="fcc1c-130">WebApp Slot Name</span></span>

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

### <span data-ttu-id="fcc1c-131">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="fcc1c-131">-StorageAccountUrl</span></span>
<span data-ttu-id="fcc1c-132">URL för lagrings konto</span><span class="sxs-lookup"><span data-stu-id="fcc1c-132">Storage Account Url</span></span>

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

### <span data-ttu-id="fcc1c-133">-WebApp</span><span class="sxs-lookup"><span data-stu-id="fcc1c-133">-WebApp</span></span>
<span data-ttu-id="fcc1c-134">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="fcc1c-134">WebApp Object</span></span>

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

### <span data-ttu-id="fcc1c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcc1c-135">CommonParameters</span></span>
<span data-ttu-id="fcc1c-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fcc1c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcc1c-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fcc1c-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcc1c-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fcc1c-138">INPUTS</span></span>

### <span data-ttu-id="fcc1c-139">System. String</span><span class="sxs-lookup"><span data-stu-id="fcc1c-139">System.String</span></span>

### <span data-ttu-id="fcc1c-140">Microsoft. Azure. Management. webbplatser. Models. DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="fcc1c-140">Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting[]</span></span>

### <span data-ttu-id="fcc1c-141">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="fcc1c-141">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="fcc1c-142">Microsoft. Azure. commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="fcc1c-142">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="fcc1c-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fcc1c-143">OUTPUTS</span></span>

### <span data-ttu-id="fcc1c-144">System. Void</span><span class="sxs-lookup"><span data-stu-id="fcc1c-144">System.Void</span></span>

## <span data-ttu-id="fcc1c-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fcc1c-145">NOTES</span></span>

## <span data-ttu-id="fcc1c-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fcc1c-146">RELATED LINKS</span></span>
