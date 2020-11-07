---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: D3FE0440-C663-4379-8F5F-2E66EF024E5D
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/new-Azwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/New-AzWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/New-AzWebAppBackup.md
ms.openlocfilehash: a01c49ac6591cfec7d8087d664ba61ddd825ac5e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923330"
---
# <span data-ttu-id="ff137-101">New-AzWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="ff137-101">New-AzWebAppBackup</span></span>

## <span data-ttu-id="ff137-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ff137-102">SYNOPSIS</span></span>

## <span data-ttu-id="ff137-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ff137-103">SYNTAX</span></span>

### <span data-ttu-id="ff137-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="ff137-104">FromResourceName</span></span>
```
New-AzWebAppBackup [[-BackupName] <String>] [-ResourceGroupName] <String> [-Name] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String>
 [-Databases <DatabaseBackupSetting[]>] [<CommonParameters>]
```

### <span data-ttu-id="ff137-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="ff137-105">FromWebApp</span></span>
```
New-AzWebAppBackup [[-BackupName] <String>] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [-Databases <DatabaseBackupSetting[]>] [<CommonParameters>]
```

## <span data-ttu-id="ff137-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ff137-106">DESCRIPTION</span></span>
<span data-ttu-id="ff137-107">Cmdleten **New-AzWebAppBackup** skapar en Azure Web App-säkerhetskopiering.</span><span class="sxs-lookup"><span data-stu-id="ff137-107">The **New-AzWebAppBackup** cmdlet creates an Azure Web App Backup.</span></span>

## <span data-ttu-id="ff137-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ff137-108">EXAMPLES</span></span>

### <span data-ttu-id="ff137-109">9.1</span><span class="sxs-lookup"><span data-stu-id="ff137-109">1:</span></span>
```
PS C:\> New-AzWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StorageAccountUrl "https://storageaccount.file.core.windows.net"
```

<span data-ttu-id="ff137-110">Skapar en säkerhets kopia av den angivna app-ContosoWebApp som ingår i resurs gruppens standard-väst i https://storageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="ff137-110">Creates a backup of the specified app ContosoWebApp that is within resource group Default-Web-WestUS in https://storageaccount.file.core.windows.net</span></span>

## <span data-ttu-id="ff137-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ff137-111">PARAMETERS</span></span>

### <span data-ttu-id="ff137-112">-BackupName</span><span class="sxs-lookup"><span data-stu-id="ff137-112">-BackupName</span></span>
<span data-ttu-id="ff137-113">Namn på säkerhets kopia</span><span class="sxs-lookup"><span data-stu-id="ff137-113">Backup Name</span></span>

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

### <span data-ttu-id="ff137-114">-Databaser</span><span class="sxs-lookup"><span data-stu-id="ff137-114">-Databases</span></span>
<span data-ttu-id="ff137-115">Databaser av typen DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="ff137-115">Databases of type DatabaseBackupSetting[]</span></span>

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

### <span data-ttu-id="ff137-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff137-116">-DefaultProfile</span></span>
<span data-ttu-id="ff137-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ff137-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ff137-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="ff137-118">-Name</span></span>
<span data-ttu-id="ff137-119">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="ff137-119">WebApp Name</span></span>

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

### <span data-ttu-id="ff137-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff137-120">-ResourceGroupName</span></span>
<span data-ttu-id="ff137-121">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="ff137-121">Resource Group Name</span></span>

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

### <span data-ttu-id="ff137-122">-Plats</span><span class="sxs-lookup"><span data-stu-id="ff137-122">-Slot</span></span>
<span data-ttu-id="ff137-123">WebApp-slot</span><span class="sxs-lookup"><span data-stu-id="ff137-123">WebApp Slot Name</span></span>

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

### <span data-ttu-id="ff137-124">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="ff137-124">-StorageAccountUrl</span></span>
<span data-ttu-id="ff137-125">URL för lagrings konto</span><span class="sxs-lookup"><span data-stu-id="ff137-125">Storage Account Url</span></span>

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

### <span data-ttu-id="ff137-126">-WebApp</span><span class="sxs-lookup"><span data-stu-id="ff137-126">-WebApp</span></span>
<span data-ttu-id="ff137-127">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="ff137-127">WebApp Object</span></span>

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

### <span data-ttu-id="ff137-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff137-128">CommonParameters</span></span>
<span data-ttu-id="ff137-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff137-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff137-130">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff137-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff137-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ff137-131">INPUTS</span></span>

### <span data-ttu-id="ff137-132">Webbplatsmallar</span><span class="sxs-lookup"><span data-stu-id="ff137-132">Site</span></span>
<span data-ttu-id="ff137-133">Parametern ' WebApp ' godkänner värdet av typen ' site ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="ff137-133">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="ff137-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ff137-134">OUTPUTS</span></span>

### <span data-ttu-id="ff137-135">Microsoft. Azure. kommandon. webapps. cmdletar. webapps. AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="ff137-135">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="ff137-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ff137-136">NOTES</span></span>

## <span data-ttu-id="ff137-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ff137-137">RELATED LINKS</span></span>

