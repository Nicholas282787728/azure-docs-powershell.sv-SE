---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: D3FE0440-C663-4379-8F5F-2E66EF024E5D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/new-azurermwebappbackup
schema: 2.0.0
ms.openlocfilehash: 7245697cab6184aa5fc2f7c292875f96cf3de3fb
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929549"
---
# <span data-ttu-id="ada04-101">New-AzureRmWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="ada04-101">New-AzureRmWebAppBackup</span></span>

## <span data-ttu-id="ada04-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ada04-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ada04-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ada04-103">SYNTAX</span></span>

### <span data-ttu-id="ada04-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="ada04-104">FromResourceName</span></span>
```
New-AzureRmWebAppBackup [[-BackupName] <String>] [-ResourceGroupName] <String> [-Name] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String>
 [-Databases <DatabaseBackupSetting[]>] [<CommonParameters>]
```

### <span data-ttu-id="ada04-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="ada04-105">FromWebApp</span></span>
```
New-AzureRmWebAppBackup [[-BackupName] <String>] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [-Databases <DatabaseBackupSetting[]>] [<CommonParameters>]
```

## <span data-ttu-id="ada04-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ada04-106">DESCRIPTION</span></span>
<span data-ttu-id="ada04-107">Cmdleten **New-AzureRmWebAppBackup** skapar en Azure Web App-säkerhetskopiering.</span><span class="sxs-lookup"><span data-stu-id="ada04-107">The **New-AzureRmWebAppBackup** cmdlet creates an Azure Web App Backup.</span></span>

## <span data-ttu-id="ada04-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ada04-108">EXAMPLES</span></span>

### <span data-ttu-id="ada04-109">9.1</span><span class="sxs-lookup"><span data-stu-id="ada04-109">1:</span></span>
```
PS C:\> New-AzureRmWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StorageAccountUrl "https://storageaccount.file.core.windows.net"
```

<span data-ttu-id="ada04-110">Skapar en säkerhets kopia av den angivna app-ContosoWebApp som ingår i resurs gruppens standard-väst i https://storageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="ada04-110">Creates a backup of the specified app ContosoWebApp that is within resource group Default-Web-WestUS in https://storageaccount.file.core.windows.net</span></span>

## <span data-ttu-id="ada04-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ada04-111">PARAMETERS</span></span>

### <span data-ttu-id="ada04-112">-BackupName</span><span class="sxs-lookup"><span data-stu-id="ada04-112">-BackupName</span></span>
<span data-ttu-id="ada04-113">Namn på säkerhets kopia</span><span class="sxs-lookup"><span data-stu-id="ada04-113">Backup Name</span></span>

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

### <span data-ttu-id="ada04-114">-Databaser</span><span class="sxs-lookup"><span data-stu-id="ada04-114">-Databases</span></span>
<span data-ttu-id="ada04-115">Databaser av typen DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="ada04-115">Databases of type DatabaseBackupSetting[]</span></span>

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

### <span data-ttu-id="ada04-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ada04-116">-DefaultProfile</span></span>
<span data-ttu-id="ada04-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ada04-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ada04-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="ada04-118">-Name</span></span>
<span data-ttu-id="ada04-119">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="ada04-119">WebApp Name</span></span>

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

### <span data-ttu-id="ada04-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ada04-120">-ResourceGroupName</span></span>
<span data-ttu-id="ada04-121">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="ada04-121">Resource Group Name</span></span>

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

### <span data-ttu-id="ada04-122">-Plats</span><span class="sxs-lookup"><span data-stu-id="ada04-122">-Slot</span></span>
<span data-ttu-id="ada04-123">WebApp-slot</span><span class="sxs-lookup"><span data-stu-id="ada04-123">WebApp Slot Name</span></span>

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

### <span data-ttu-id="ada04-124">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="ada04-124">-StorageAccountUrl</span></span>
<span data-ttu-id="ada04-125">URL för lagrings konto</span><span class="sxs-lookup"><span data-stu-id="ada04-125">Storage Account Url</span></span>

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

### <span data-ttu-id="ada04-126">-WebApp</span><span class="sxs-lookup"><span data-stu-id="ada04-126">-WebApp</span></span>
<span data-ttu-id="ada04-127">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="ada04-127">WebApp Object</span></span>

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

### <span data-ttu-id="ada04-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ada04-128">CommonParameters</span></span>
<span data-ttu-id="ada04-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ada04-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ada04-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ada04-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ada04-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ada04-131">INPUTS</span></span>

### <span data-ttu-id="ada04-132">Webbplatsmallar</span><span class="sxs-lookup"><span data-stu-id="ada04-132">Site</span></span>
<span data-ttu-id="ada04-133">Parametern ' WebApp ' godkänner värdet av typen ' site ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="ada04-133">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="ada04-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ada04-134">OUTPUTS</span></span>

### <span data-ttu-id="ada04-135">Microsoft. Azure. kommandon. webapps. cmdletar. webapps. AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="ada04-135">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="ada04-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ada04-136">NOTES</span></span>

## <span data-ttu-id="ada04-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ada04-137">RELATED LINKS</span></span>

