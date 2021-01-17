---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: EAAF615B-6139-438B-A2FD-6966E72B3AA9
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackup.md
ms.openlocfilehash: e8c3f7543062613527e7f52be2cd6493f53c5f60
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98422648"
---
# <span data-ttu-id="e653c-101">Get-AzWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="e653c-101">Get-AzWebAppBackup</span></span>

## <span data-ttu-id="e653c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e653c-102">SYNOPSIS</span></span>

## <span data-ttu-id="e653c-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e653c-103">SYNTAX</span></span>

### <span data-ttu-id="e653c-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="e653c-104">FromResourceName</span></span>
```
Get-AzWebAppBackup [-BackupId] <String> [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e653c-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="e653c-105">FromWebApp</span></span>
```
Get-AzWebAppBackup [-BackupId] <String> [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e653c-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e653c-106">DESCRIPTION</span></span>
<span data-ttu-id="e653c-107">Cmdleten **Get-AzWebAppBackup** hämtar den angivna säkerhets kopian av ett Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="e653c-107">The **Get-AzWebAppBackup** cmdlet gets the specified backup of an Azure Web App.</span></span>

## <span data-ttu-id="e653c-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e653c-108">EXAMPLES</span></span>

### <span data-ttu-id="e653c-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e653c-109">Example 1</span></span>
```powershell
PS C:\>Get-AzWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -BackupId "12345"
```

<span data-ttu-id="e653c-110">Med det här kommandot får du säkerhets kopian med ID: t "12345" från webb programmet som heter WebAppStandard som tillhör resurs gruppens standard-väst.</span><span class="sxs-lookup"><span data-stu-id="e653c-110">This command gets the backup with ID "12345" from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="e653c-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e653c-111">PARAMETERS</span></span>

### <span data-ttu-id="e653c-112">-BackupId</span><span class="sxs-lookup"><span data-stu-id="e653c-112">-BackupId</span></span>
<span data-ttu-id="e653c-113">Säkerhets kopie-ID</span><span class="sxs-lookup"><span data-stu-id="e653c-113">Backup Id</span></span>

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

### <span data-ttu-id="e653c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e653c-114">-DefaultProfile</span></span>
<span data-ttu-id="e653c-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e653c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e653c-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="e653c-116">-Name</span></span>
<span data-ttu-id="e653c-117">Webapp-namn</span><span class="sxs-lookup"><span data-stu-id="e653c-117">Webapp Name</span></span>

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

### <span data-ttu-id="e653c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e653c-118">-ResourceGroupName</span></span>
<span data-ttu-id="e653c-119">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="e653c-119">Resource Group Name</span></span>

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

### <span data-ttu-id="e653c-120">-Plats</span><span class="sxs-lookup"><span data-stu-id="e653c-120">-Slot</span></span>
<span data-ttu-id="e653c-121">Plats namn</span><span class="sxs-lookup"><span data-stu-id="e653c-121">Slot Name</span></span>

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

### <span data-ttu-id="e653c-122">-WebApp</span><span class="sxs-lookup"><span data-stu-id="e653c-122">-WebApp</span></span>
<span data-ttu-id="e653c-123">Piped WebApp</span><span class="sxs-lookup"><span data-stu-id="e653c-123">Piped WebApp</span></span>

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

### <span data-ttu-id="e653c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e653c-124">CommonParameters</span></span>
<span data-ttu-id="e653c-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e653c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e653c-126">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e653c-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e653c-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e653c-127">INPUTS</span></span>

### <span data-ttu-id="e653c-128">System. String</span><span class="sxs-lookup"><span data-stu-id="e653c-128">System.String</span></span>

### <span data-ttu-id="e653c-129">Microsoft. Azure. commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="e653c-129">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="e653c-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e653c-130">OUTPUTS</span></span>

### <span data-ttu-id="e653c-131">Microsoft. Azure. kommandon. webapps. cmdletar. webapps. AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="e653c-131">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="e653c-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e653c-132">NOTES</span></span>

## <span data-ttu-id="e653c-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e653c-133">RELATED LINKS</span></span>
