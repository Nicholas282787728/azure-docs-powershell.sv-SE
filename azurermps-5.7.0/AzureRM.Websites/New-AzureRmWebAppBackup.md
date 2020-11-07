---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: D3FE0440-C663-4379-8F5F-2E66EF024E5D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/new-azurermwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppBackup.md
ms.openlocfilehash: 7784ea832faef9f73b46b04d6ad36bebe0e2f36d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580911"
---
# <span data-ttu-id="d40bb-101">New-AzureRmWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="d40bb-101">New-AzureRmWebAppBackup</span></span>

## <span data-ttu-id="d40bb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d40bb-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d40bb-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d40bb-103">SYNTAX</span></span>

### <span data-ttu-id="d40bb-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="d40bb-104">FromResourceName</span></span>
```
New-AzureRmWebAppBackup [[-BackupName] <String>] [-ResourceGroupName] <String> [-Name] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String>
 [-Databases <DatabaseBackupSetting[]>] [<CommonParameters>]
```

### <span data-ttu-id="d40bb-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="d40bb-105">FromWebApp</span></span>
```
New-AzureRmWebAppBackup [[-BackupName] <String>] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [-Databases <DatabaseBackupSetting[]>] [<CommonParameters>]
```

## <span data-ttu-id="d40bb-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d40bb-106">DESCRIPTION</span></span>
<span data-ttu-id="d40bb-107">Cmdleten **New-AzureRmWebAppBackup** skapar en Azure Web App-säkerhetskopiering.</span><span class="sxs-lookup"><span data-stu-id="d40bb-107">The **New-AzureRmWebAppBackup** cmdlet creates an Azure Web App Backup.</span></span>

## <span data-ttu-id="d40bb-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d40bb-108">EXAMPLES</span></span>

### <span data-ttu-id="d40bb-109">9.1</span><span class="sxs-lookup"><span data-stu-id="d40bb-109">1:</span></span>
```
PS C:\> New-AzureRmWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StorageAccountUrl "https://storageaccount.file.core.windows.net"
```

<span data-ttu-id="d40bb-110">Skapar en säkerhets kopia av den angivna app-ContosoWebApp som ingår i resurs gruppens standard-väst i https://storageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="d40bb-110">Creates a backup of the specified app ContosoWebApp that is within resource group Default-Web-WestUS in https://storageaccount.file.core.windows.net</span></span>

## <span data-ttu-id="d40bb-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d40bb-111">PARAMETERS</span></span>

### <span data-ttu-id="d40bb-112">-BackupName</span><span class="sxs-lookup"><span data-stu-id="d40bb-112">-BackupName</span></span>
<span data-ttu-id="d40bb-113">Namn på säkerhets kopia</span><span class="sxs-lookup"><span data-stu-id="d40bb-113">Backup Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d40bb-114">-Databaser</span><span class="sxs-lookup"><span data-stu-id="d40bb-114">-Databases</span></span>
<span data-ttu-id="d40bb-115">Databaser av typen DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="d40bb-115">Databases of type DatabaseBackupSetting[]</span></span>

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

### <span data-ttu-id="d40bb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d40bb-116">-DefaultProfile</span></span>
<span data-ttu-id="d40bb-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d40bb-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d40bb-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="d40bb-118">-Name</span></span>
<span data-ttu-id="d40bb-119">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="d40bb-119">WebApp Name</span></span>

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

### <span data-ttu-id="d40bb-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d40bb-120">-ResourceGroupName</span></span>
<span data-ttu-id="d40bb-121">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="d40bb-121">Resource Group Name</span></span>

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

### <span data-ttu-id="d40bb-122">-Plats</span><span class="sxs-lookup"><span data-stu-id="d40bb-122">-Slot</span></span>
<span data-ttu-id="d40bb-123">WebApp-slot</span><span class="sxs-lookup"><span data-stu-id="d40bb-123">WebApp Slot Name</span></span>

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

### <span data-ttu-id="d40bb-124">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="d40bb-124">-StorageAccountUrl</span></span>
<span data-ttu-id="d40bb-125">URL för lagrings konto</span><span class="sxs-lookup"><span data-stu-id="d40bb-125">Storage Account Url</span></span>

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

### <span data-ttu-id="d40bb-126">-WebApp</span><span class="sxs-lookup"><span data-stu-id="d40bb-126">-WebApp</span></span>
<span data-ttu-id="d40bb-127">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="d40bb-127">WebApp Object</span></span>

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

### <span data-ttu-id="d40bb-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d40bb-128">CommonParameters</span></span>
<span data-ttu-id="d40bb-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d40bb-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d40bb-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d40bb-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d40bb-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d40bb-131">INPUTS</span></span>

### <span data-ttu-id="d40bb-132">Webbplatsmallar</span><span class="sxs-lookup"><span data-stu-id="d40bb-132">Site</span></span>
<span data-ttu-id="d40bb-133">Parametern ' WebApp ' godkänner värdet av typen ' site ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="d40bb-133">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="d40bb-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d40bb-134">OUTPUTS</span></span>

### <span data-ttu-id="d40bb-135">Microsoft. Azure. kommandon. webapps. cmdletar. webapps. AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="d40bb-135">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="d40bb-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d40bb-136">NOTES</span></span>

## <span data-ttu-id="d40bb-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d40bb-137">RELATED LINKS</span></span>
