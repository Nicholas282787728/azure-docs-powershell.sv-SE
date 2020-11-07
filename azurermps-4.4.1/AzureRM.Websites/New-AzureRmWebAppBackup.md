---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: D3FE0440-C663-4379-8F5F-2E66EF024E5D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppBackup.md
ms.openlocfilehash: 03c9b54dd83f4689f763ef45e0f9a7c0d8b89672
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757977"
---
# <span data-ttu-id="d7d4e-101">New-AzureRmWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="d7d4e-101">New-AzureRmWebAppBackup</span></span>

## <span data-ttu-id="d7d4e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d7d4e-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7d4e-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d7d4e-103">SYNTAX</span></span>

### <span data-ttu-id="d7d4e-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="d7d4e-104">FromResourceName</span></span>
```
New-AzureRmWebAppBackup [[-BackupName] <String>] [-ResourceGroupName] <String> [-Name] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String>
 [-Databases <DatabaseBackupSetting[]>] [<CommonParameters>]
```

### <span data-ttu-id="d7d4e-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="d7d4e-105">FromWebApp</span></span>
```
New-AzureRmWebAppBackup [[-BackupName] <String>] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [-Databases <DatabaseBackupSetting[]>] [<CommonParameters>]
```

## <span data-ttu-id="d7d4e-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d7d4e-106">DESCRIPTION</span></span>
<span data-ttu-id="d7d4e-107">Cmdleten **New-AzureRmWebAppBackup** skapar en Azure Web App-säkerhetskopiering.</span><span class="sxs-lookup"><span data-stu-id="d7d4e-107">The **New-AzureRmWebAppBackup** cmdlet creates an Azure Web App Backup.</span></span>

## <span data-ttu-id="d7d4e-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d7d4e-108">EXAMPLES</span></span>

### <span data-ttu-id="d7d4e-109">9.1</span><span class="sxs-lookup"><span data-stu-id="d7d4e-109">1:</span></span>
```
PS C:\> New-AzureRmWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StorageAccountUrl "https://storageaccount.file.core.windows.net"
```

<span data-ttu-id="d7d4e-110">Skapar en säkerhets kopia av den angivna app-ContosoWebApp som ingår i resurs gruppens standard-väst i https://storageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="d7d4e-110">Creates a backup of the specified app ContosoWebApp that is within resource group Default-Web-WestUS in https://storageaccount.file.core.windows.net</span></span>

## <span data-ttu-id="d7d4e-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d7d4e-111">PARAMETERS</span></span>

### <span data-ttu-id="d7d4e-112">-BackupName</span><span class="sxs-lookup"><span data-stu-id="d7d4e-112">-BackupName</span></span>
<span data-ttu-id="d7d4e-113">Namn på säkerhets kopia</span><span class="sxs-lookup"><span data-stu-id="d7d4e-113">Backup Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7d4e-114">-Databaser</span><span class="sxs-lookup"><span data-stu-id="d7d4e-114">-Databases</span></span>
<span data-ttu-id="d7d4e-115">Databaser av typen DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="d7d4e-115">Databases of type DatabaseBackupSetting[]</span></span>

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

### <span data-ttu-id="d7d4e-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="d7d4e-116">-Name</span></span>
<span data-ttu-id="d7d4e-117">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="d7d4e-117">WebApp Name</span></span>

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

### <span data-ttu-id="d7d4e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7d4e-118">-ResourceGroupName</span></span>
<span data-ttu-id="d7d4e-119">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="d7d4e-119">Resource Group Name</span></span>

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

### <span data-ttu-id="d7d4e-120">-Plats</span><span class="sxs-lookup"><span data-stu-id="d7d4e-120">-Slot</span></span>
<span data-ttu-id="d7d4e-121">WebApp-slot</span><span class="sxs-lookup"><span data-stu-id="d7d4e-121">WebApp Slot Name</span></span>

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

### <span data-ttu-id="d7d4e-122">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="d7d4e-122">-StorageAccountUrl</span></span>
<span data-ttu-id="d7d4e-123">URL för lagrings konto</span><span class="sxs-lookup"><span data-stu-id="d7d4e-123">Storage Account Url</span></span>

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

### <span data-ttu-id="d7d4e-124">-WebApp</span><span class="sxs-lookup"><span data-stu-id="d7d4e-124">-WebApp</span></span>
<span data-ttu-id="d7d4e-125">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="d7d4e-125">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: FromWebApp
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d7d4e-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7d4e-126">-DefaultProfile</span></span>
<span data-ttu-id="d7d4e-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d7d4e-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d7d4e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7d4e-128">CommonParameters</span></span>
<span data-ttu-id="d7d4e-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7d4e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7d4e-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7d4e-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7d4e-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d7d4e-131">INPUTS</span></span>

### <span data-ttu-id="d7d4e-132">Webbplatsmallar</span><span class="sxs-lookup"><span data-stu-id="d7d4e-132">Site</span></span>
<span data-ttu-id="d7d4e-133">Parametern ' WebApp ' godkänner värdet av typen ' site ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="d7d4e-133">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="d7d4e-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d7d4e-134">OUTPUTS</span></span>

### <span data-ttu-id="d7d4e-135">Microsoft. Azure. kommandon. webapps. cmdletar. webapps. AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="d7d4e-135">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="d7d4e-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d7d4e-136">NOTES</span></span>

## <span data-ttu-id="d7d4e-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d7d4e-137">RELATED LINKS</span></span>

