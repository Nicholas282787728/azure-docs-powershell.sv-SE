---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: DC400E32-CAB9-4354-99B2-ABA4AA776030
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/restore-azurermwebappbackup
schema: 2.0.0
ms.openlocfilehash: 9c28d9235eefe6c4f33537115b548137c5bc6c88
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930782"
---
# <span data-ttu-id="35ecf-101">Restore-AzureRmWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="35ecf-101">Restore-AzureRmWebAppBackup</span></span>

## <span data-ttu-id="35ecf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="35ecf-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="35ecf-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="35ecf-103">SYNTAX</span></span>

### <span data-ttu-id="35ecf-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="35ecf-104">FromResourceName</span></span>
```
Restore-AzureRmWebAppBackup [-AppServicePlan <String>] [-Databases <DatabaseBackupSetting[]>]
 [-IgnoreConflictingHostNames] [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String> [-BlobName] <String> [-Overwrite]
 [<CommonParameters>]
```

### <span data-ttu-id="35ecf-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="35ecf-105">FromWebApp</span></span>
```
Restore-AzureRmWebAppBackup [-AppServicePlan <String>] [-Databases <DatabaseBackupSetting[]>]
 [-IgnoreConflictingHostNames] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [-BlobName] <String> [-Overwrite] [<CommonParameters>]
```

## <span data-ttu-id="35ecf-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="35ecf-106">DESCRIPTION</span></span>
<span data-ttu-id="35ecf-107">Cmdleten **restore-AzureRmWebAppBackup** återställer en Azure Web App-säkerhetskopia.</span><span class="sxs-lookup"><span data-stu-id="35ecf-107">The **Restore-AzureRmWebAppBackup** cmdlet restores an Azure Web App Backup.</span></span>

## <span data-ttu-id="35ecf-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="35ecf-108">EXAMPLES</span></span>

### <span data-ttu-id="35ecf-109">9.1</span><span class="sxs-lookup"><span data-stu-id="35ecf-109">1:</span></span>
```
PS C:\> Restore-AzureRmWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StorageAccountUrl "https://storageaccount.file.core.windows.net" -BlobName "myBlob"
```

<span data-ttu-id="35ecf-110">Återställer en säkerhets kopia av den angivna app-ContosoWebApp som ingår i resurs gruppens standardinställning-väst i BLOB "mittArkiv" på https://storageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="35ecf-110">Restores a backup of the specified app ContosoWebApp that is within resource group Default-Web-WestUS in blob "myBlob" located at https://storageaccount.file.core.windows.net</span></span>

## <span data-ttu-id="35ecf-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="35ecf-111">PARAMETERS</span></span>

### <span data-ttu-id="35ecf-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="35ecf-112">-AppServicePlan</span></span>
<span data-ttu-id="35ecf-113">Namnet på App Service-planen för det återställda programmet.</span><span class="sxs-lookup"><span data-stu-id="35ecf-113">The name of the App Service Plan for the restored app.</span></span> <span data-ttu-id="35ecf-114">Om du lämnar det här alternativet används appens nuvarande App Service-plan.</span><span class="sxs-lookup"><span data-stu-id="35ecf-114">If left empty, the app's current App Service Plan is used.</span></span>
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

### <span data-ttu-id="35ecf-115">-BlobName</span><span class="sxs-lookup"><span data-stu-id="35ecf-115">-BlobName</span></span>
<span data-ttu-id="35ecf-116">BLOB-namn</span><span class="sxs-lookup"><span data-stu-id="35ecf-116">Blob Name</span></span>

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

### <span data-ttu-id="35ecf-117">-Databaser</span><span class="sxs-lookup"><span data-stu-id="35ecf-117">-Databases</span></span>
<span data-ttu-id="35ecf-118">Databaser av typen DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="35ecf-118">Databases of type DatabaseBackupSetting[]</span></span>

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

### <span data-ttu-id="35ecf-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35ecf-119">-DefaultProfile</span></span>
<span data-ttu-id="35ecf-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="35ecf-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35ecf-121">-IgnoreConflictingHostNames</span><span class="sxs-lookup"><span data-stu-id="35ecf-121">-IgnoreConflictingHostNames</span></span>
<span data-ttu-id="35ecf-122">Ignorera alternativ för värdbaserade namn</span><span class="sxs-lookup"><span data-stu-id="35ecf-122">Ignore Conflicting HostNames Option</span></span>

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

### <span data-ttu-id="35ecf-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="35ecf-123">-Name</span></span>
<span data-ttu-id="35ecf-124">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="35ecf-124">WebApp Name</span></span>

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

### <span data-ttu-id="35ecf-125">-Skriver över</span><span class="sxs-lookup"><span data-stu-id="35ecf-125">-Overwrite</span></span>
<span data-ttu-id="35ecf-126">Alternativet överskrivning</span><span class="sxs-lookup"><span data-stu-id="35ecf-126">Overwrite Option</span></span>

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

### <span data-ttu-id="35ecf-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35ecf-127">-ResourceGroupName</span></span>
<span data-ttu-id="35ecf-128">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="35ecf-128">Resource Group Name</span></span>

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

### <span data-ttu-id="35ecf-129">-Plats</span><span class="sxs-lookup"><span data-stu-id="35ecf-129">-Slot</span></span>
<span data-ttu-id="35ecf-130">WebApp-slot</span><span class="sxs-lookup"><span data-stu-id="35ecf-130">WebApp Slot Name</span></span>

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

### <span data-ttu-id="35ecf-131">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="35ecf-131">-StorageAccountUrl</span></span>
<span data-ttu-id="35ecf-132">URL för lagrings konto</span><span class="sxs-lookup"><span data-stu-id="35ecf-132">Storage Account Url</span></span>

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

### <span data-ttu-id="35ecf-133">-WebApp</span><span class="sxs-lookup"><span data-stu-id="35ecf-133">-WebApp</span></span>
<span data-ttu-id="35ecf-134">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="35ecf-134">WebApp Object</span></span>

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

### <span data-ttu-id="35ecf-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35ecf-135">CommonParameters</span></span>
<span data-ttu-id="35ecf-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35ecf-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35ecf-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35ecf-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35ecf-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="35ecf-138">INPUTS</span></span>

### <span data-ttu-id="35ecf-139">Webbplatsmallar</span><span class="sxs-lookup"><span data-stu-id="35ecf-139">Site</span></span>
<span data-ttu-id="35ecf-140">Parametern ' WebApp ' godkänner värdet av typen ' site ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="35ecf-140">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="35ecf-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="35ecf-141">OUTPUTS</span></span>

## <span data-ttu-id="35ecf-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="35ecf-142">NOTES</span></span>

## <span data-ttu-id="35ecf-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="35ecf-143">RELATED LINKS</span></span>

