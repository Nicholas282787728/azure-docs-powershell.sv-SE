---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: D3FE0440-C663-4379-8F5F-2E66EF024E5D
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppBackup.md
ms.openlocfilehash: 2ef015c3f793dd4636632f17568feb9aaf1b5ad2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746059"
---
# <span data-ttu-id="c59ac-101">New-AzWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="c59ac-101">New-AzWebAppBackup</span></span>

## <span data-ttu-id="c59ac-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c59ac-102">SYNOPSIS</span></span>

## <span data-ttu-id="c59ac-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c59ac-103">SYNTAX</span></span>

### <span data-ttu-id="c59ac-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="c59ac-104">FromResourceName</span></span>
```
New-AzWebAppBackup [[-BackupName] <String>] [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String>
 [-Databases <DatabaseBackupSetting[]>] [<CommonParameters>]
```

### <span data-ttu-id="c59ac-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="c59ac-105">FromWebApp</span></span>
```
New-AzWebAppBackup [[-BackupName] <String>] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [-Databases <DatabaseBackupSetting[]>] [<CommonParameters>]
```

## <span data-ttu-id="c59ac-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c59ac-106">DESCRIPTION</span></span>
<span data-ttu-id="c59ac-107">Cmdleten **New-AzWebAppBackup** skapar en Azure Web App-säkerhetskopiering.</span><span class="sxs-lookup"><span data-stu-id="c59ac-107">The **New-AzWebAppBackup** cmdlet creates an Azure Web App Backup.</span></span>

## <span data-ttu-id="c59ac-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c59ac-108">EXAMPLES</span></span>

### <span data-ttu-id="c59ac-109">9.1</span><span class="sxs-lookup"><span data-stu-id="c59ac-109">1:</span></span>
```
PS C:\> New-AzWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StorageAccountUrl "https://storageaccount.file.core.windows.net"
```

<span data-ttu-id="c59ac-110">Skapar en säkerhets kopia av den angivna app-ContosoWebApp som ingår i resurs gruppens standard-väst i https://storageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="c59ac-110">Creates a backup of the specified app ContosoWebApp that is within resource group Default-Web-WestUS in https://storageaccount.file.core.windows.net</span></span>

## <span data-ttu-id="c59ac-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c59ac-111">PARAMETERS</span></span>

### <span data-ttu-id="c59ac-112">-BackupName</span><span class="sxs-lookup"><span data-stu-id="c59ac-112">-BackupName</span></span>
<span data-ttu-id="c59ac-113">Namn på säkerhets kopia</span><span class="sxs-lookup"><span data-stu-id="c59ac-113">Backup Name</span></span>

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

### <span data-ttu-id="c59ac-114">-Databaser</span><span class="sxs-lookup"><span data-stu-id="c59ac-114">-Databases</span></span>
<span data-ttu-id="c59ac-115">Databaser av typen DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="c59ac-115">Databases of type DatabaseBackupSetting[]</span></span>

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

### <span data-ttu-id="c59ac-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c59ac-116">-DefaultProfile</span></span>
<span data-ttu-id="c59ac-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c59ac-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c59ac-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="c59ac-118">-Name</span></span>
<span data-ttu-id="c59ac-119">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="c59ac-119">WebApp Name</span></span>

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

### <span data-ttu-id="c59ac-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c59ac-120">-ResourceGroupName</span></span>
<span data-ttu-id="c59ac-121">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="c59ac-121">Resource Group Name</span></span>

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

### <span data-ttu-id="c59ac-122">-Plats</span><span class="sxs-lookup"><span data-stu-id="c59ac-122">-Slot</span></span>
<span data-ttu-id="c59ac-123">WebApp-slot</span><span class="sxs-lookup"><span data-stu-id="c59ac-123">WebApp Slot Name</span></span>

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

### <span data-ttu-id="c59ac-124">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="c59ac-124">-StorageAccountUrl</span></span>
<span data-ttu-id="c59ac-125">URL för lagrings konto</span><span class="sxs-lookup"><span data-stu-id="c59ac-125">Storage Account Url</span></span>

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

### <span data-ttu-id="c59ac-126">-WebApp</span><span class="sxs-lookup"><span data-stu-id="c59ac-126">-WebApp</span></span>
<span data-ttu-id="c59ac-127">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="c59ac-127">WebApp Object</span></span>

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

### <span data-ttu-id="c59ac-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c59ac-128">CommonParameters</span></span>
<span data-ttu-id="c59ac-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c59ac-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c59ac-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c59ac-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c59ac-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c59ac-131">INPUTS</span></span>

### <span data-ttu-id="c59ac-132">System. String</span><span class="sxs-lookup"><span data-stu-id="c59ac-132">System.String</span></span>

### <span data-ttu-id="c59ac-133">Microsoft. Azure. commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="c59ac-133">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

### <span data-ttu-id="c59ac-134">Microsoft. Azure. Management. webbplatser. Models. DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="c59ac-134">Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting[]</span></span>

## <span data-ttu-id="c59ac-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c59ac-135">OUTPUTS</span></span>

### <span data-ttu-id="c59ac-136">Microsoft. Azure. kommandon. webapps. cmdletar. webapps. AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="c59ac-136">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="c59ac-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c59ac-137">NOTES</span></span>

## <span data-ttu-id="c59ac-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c59ac-138">RELATED LINKS</span></span>
