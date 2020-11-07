---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: EAAF615B-6139-438B-A2FD-6966E72B3AA9
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackup.md
ms.openlocfilehash: 65748ed269a7cb42914c98549c68be32812f71f3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93926342"
---
# <span data-ttu-id="e913b-101">Get-AzWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="e913b-101">Get-AzWebAppBackup</span></span>

## <span data-ttu-id="e913b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e913b-102">SYNOPSIS</span></span>

## <span data-ttu-id="e913b-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e913b-103">SYNTAX</span></span>

### <span data-ttu-id="e913b-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="e913b-104">FromResourceName</span></span>
```
Get-AzWebAppBackup [-BackupId] <String> [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e913b-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="e913b-105">FromWebApp</span></span>
```
Get-AzWebAppBackup [-BackupId] <String> [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e913b-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e913b-106">DESCRIPTION</span></span>
<span data-ttu-id="e913b-107">Cmdleten **Get-AzWebAppBackup** hämtar den angivna säkerhets kopian av ett Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="e913b-107">The **Get-AzWebAppBackup** cmdlet gets the specified backup of an Azure Web App.</span></span>

## <span data-ttu-id="e913b-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e913b-108">EXAMPLES</span></span>

### <span data-ttu-id="e913b-109">9.1</span><span class="sxs-lookup"><span data-stu-id="e913b-109">1:</span></span>
```
PS C:\>Get-AzWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -BackupId "12345"
```

<span data-ttu-id="e913b-110">Med det här kommandot får du säkerhets kopian med ID: t "12345" från webb programmet som heter WebAppStandard som tillhör resurs gruppens standard-väst.</span><span class="sxs-lookup"><span data-stu-id="e913b-110">This command gets the backup with ID "12345" from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="e913b-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e913b-111">PARAMETERS</span></span>

### <span data-ttu-id="e913b-112">-BackupId</span><span class="sxs-lookup"><span data-stu-id="e913b-112">-BackupId</span></span>
<span data-ttu-id="e913b-113">Säkerhets kopie-ID</span><span class="sxs-lookup"><span data-stu-id="e913b-113">Backup Id</span></span>

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

### <span data-ttu-id="e913b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e913b-114">-DefaultProfile</span></span>
<span data-ttu-id="e913b-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e913b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e913b-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="e913b-116">-Name</span></span>
<span data-ttu-id="e913b-117">Webapp-namn</span><span class="sxs-lookup"><span data-stu-id="e913b-117">Webapp Name</span></span>

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

### <span data-ttu-id="e913b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e913b-118">-ResourceGroupName</span></span>
<span data-ttu-id="e913b-119">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="e913b-119">Resource Group Name</span></span>

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

### <span data-ttu-id="e913b-120">-Plats</span><span class="sxs-lookup"><span data-stu-id="e913b-120">-Slot</span></span>
<span data-ttu-id="e913b-121">Plats namn</span><span class="sxs-lookup"><span data-stu-id="e913b-121">Slot Name</span></span>

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

### <span data-ttu-id="e913b-122">-WebApp</span><span class="sxs-lookup"><span data-stu-id="e913b-122">-WebApp</span></span>
<span data-ttu-id="e913b-123">Piped WebApp</span><span class="sxs-lookup"><span data-stu-id="e913b-123">Piped WebApp</span></span>

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

### <span data-ttu-id="e913b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e913b-124">CommonParameters</span></span>
<span data-ttu-id="e913b-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e913b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e913b-126">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e913b-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e913b-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e913b-127">INPUTS</span></span>

### <span data-ttu-id="e913b-128">System. String</span><span class="sxs-lookup"><span data-stu-id="e913b-128">System.String</span></span>

### <span data-ttu-id="e913b-129">Microsoft. Azure. commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="e913b-129">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="e913b-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e913b-130">OUTPUTS</span></span>

### <span data-ttu-id="e913b-131">Microsoft. Azure. kommandon. webapps. cmdletar. webapps. AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="e913b-131">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="e913b-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e913b-132">NOTES</span></span>

## <span data-ttu-id="e913b-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e913b-133">RELATED LINKS</span></span>
