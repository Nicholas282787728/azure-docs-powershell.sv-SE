---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: DC400E32-CAB9-4354-99B2-ABA4AA776030
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/restore-Azwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Restore-AzWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Restore-AzWebAppBackup.md
ms.openlocfilehash: f93a173e79cb34c5603ce58fc3e03c92869a5d01
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923262"
---
# <span data-ttu-id="b9458-101">Restore-AzWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="b9458-101">Restore-AzWebAppBackup</span></span>

## <span data-ttu-id="b9458-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b9458-102">SYNOPSIS</span></span>

## <span data-ttu-id="b9458-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b9458-103">SYNTAX</span></span>

### <span data-ttu-id="b9458-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="b9458-104">FromResourceName</span></span>
```
Restore-AzWebAppBackup [-AppServicePlan <String>] [-Databases <DatabaseBackupSetting[]>]
 [-IgnoreConflictingHostNames] [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String> [-BlobName] <String> [-Overwrite]
 [<CommonParameters>]
```

### <span data-ttu-id="b9458-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="b9458-105">FromWebApp</span></span>
```
Restore-AzWebAppBackup [-AppServicePlan <String>] [-Databases <DatabaseBackupSetting[]>]
 [-IgnoreConflictingHostNames] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [-BlobName] <String> [-Overwrite] [<CommonParameters>]
```

## <span data-ttu-id="b9458-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b9458-106">DESCRIPTION</span></span>
<span data-ttu-id="b9458-107">Cmdleten **restore-AzWebAppBackup** återställer en Azure Web App-säkerhetskopia.</span><span class="sxs-lookup"><span data-stu-id="b9458-107">The **Restore-AzWebAppBackup** cmdlet restores an Azure Web App Backup.</span></span>

## <span data-ttu-id="b9458-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b9458-108">EXAMPLES</span></span>

### <span data-ttu-id="b9458-109">9.1</span><span class="sxs-lookup"><span data-stu-id="b9458-109">1:</span></span>
```
PS C:\> Restore-AzWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StorageAccountUrl "https://storageaccount.file.core.windows.net" -BlobName "myBlob"
```

<span data-ttu-id="b9458-110">Återställer en säkerhets kopia av den angivna app-ContosoWebApp som ingår i resurs gruppens standardinställning-väst i BLOB "mittArkiv" på https://storageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="b9458-110">Restores a backup of the specified app ContosoWebApp that is within resource group Default-Web-WestUS in blob "myBlob" located at https://storageaccount.file.core.windows.net</span></span>

## <span data-ttu-id="b9458-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b9458-111">PARAMETERS</span></span>

### <span data-ttu-id="b9458-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="b9458-112">-AppServicePlan</span></span>
<span data-ttu-id="b9458-113">Namnet på App Service-planen för det återställda programmet.</span><span class="sxs-lookup"><span data-stu-id="b9458-113">The name of the App Service Plan for the restored app.</span></span> <span data-ttu-id="b9458-114">Om du lämnar det här alternativet används appens nuvarande App Service-plan.</span><span class="sxs-lookup"><span data-stu-id="b9458-114">If left empty, the app's current App Service Plan is used.</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9458-115">-BlobName</span><span class="sxs-lookup"><span data-stu-id="b9458-115">-BlobName</span></span>
<span data-ttu-id="b9458-116">BLOB-namn</span><span class="sxs-lookup"><span data-stu-id="b9458-116">Blob Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9458-117">-Databaser</span><span class="sxs-lookup"><span data-stu-id="b9458-117">-Databases</span></span>
<span data-ttu-id="b9458-118">Databaser av typen DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="b9458-118">Databases of type DatabaseBackupSetting[]</span></span>

```yaml
Type: DatabaseBackupSetting[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9458-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9458-119">-DefaultProfile</span></span>
<span data-ttu-id="b9458-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b9458-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9458-121">-IgnoreConflictingHostNames</span><span class="sxs-lookup"><span data-stu-id="b9458-121">-IgnoreConflictingHostNames</span></span>
<span data-ttu-id="b9458-122">Ignorera alternativ för värdbaserade namn</span><span class="sxs-lookup"><span data-stu-id="b9458-122">Ignore Conflicting HostNames Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9458-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="b9458-123">-Name</span></span>
<span data-ttu-id="b9458-124">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="b9458-124">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9458-125">-Skriver över</span><span class="sxs-lookup"><span data-stu-id="b9458-125">-Overwrite</span></span>
<span data-ttu-id="b9458-126">Alternativet överskrivning</span><span class="sxs-lookup"><span data-stu-id="b9458-126">Overwrite Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9458-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9458-127">-ResourceGroupName</span></span>
<span data-ttu-id="b9458-128">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="b9458-128">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9458-129">-Plats</span><span class="sxs-lookup"><span data-stu-id="b9458-129">-Slot</span></span>
<span data-ttu-id="b9458-130">WebApp-slot</span><span class="sxs-lookup"><span data-stu-id="b9458-130">WebApp Slot Name</span></span>

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9458-131">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="b9458-131">-StorageAccountUrl</span></span>
<span data-ttu-id="b9458-132">URL för lagrings konto</span><span class="sxs-lookup"><span data-stu-id="b9458-132">Storage Account Url</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9458-133">-WebApp</span><span class="sxs-lookup"><span data-stu-id="b9458-133">-WebApp</span></span>
<span data-ttu-id="b9458-134">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="b9458-134">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: FromWebApp
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b9458-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9458-135">CommonParameters</span></span>
<span data-ttu-id="b9458-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9458-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9458-137">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9458-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9458-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b9458-138">INPUTS</span></span>

### <span data-ttu-id="b9458-139">Webbplatsmallar</span><span class="sxs-lookup"><span data-stu-id="b9458-139">Site</span></span>
<span data-ttu-id="b9458-140">Parametern ' WebApp ' godkänner värdet av typen ' site ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="b9458-140">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="b9458-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b9458-141">OUTPUTS</span></span>

## <span data-ttu-id="b9458-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b9458-142">NOTES</span></span>

## <span data-ttu-id="b9458-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b9458-143">RELATED LINKS</span></span>

