---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 89ED4231-7616-47D0-BDAA-D849C245DC79
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzAppServicePlan.md
ms.openlocfilehash: afbee0d6b13c1ce42931a2379cff6aa7ee0127b9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260861"
---
# <span data-ttu-id="6fb02-101">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="6fb02-101">Get-AzAppServicePlan</span></span>

## <span data-ttu-id="6fb02-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6fb02-102">SYNOPSIS</span></span>
<span data-ttu-id="6fb02-103">Hämtar en Azure App Service-plan i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="6fb02-103">Gets an Azure App Service plan in the specified resource group.</span></span>

## <span data-ttu-id="6fb02-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6fb02-104">SYNTAX</span></span>

### <span data-ttu-id="6fb02-105">S</span><span class="sxs-lookup"><span data-stu-id="6fb02-105">S1</span></span>
```
Get-AzAppServicePlan [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6fb02-106">S2</span><span class="sxs-lookup"><span data-stu-id="6fb02-106">S2</span></span>
```
Get-AzAppServicePlan [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6fb02-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6fb02-107">DESCRIPTION</span></span>
<span data-ttu-id="6fb02-108">Cmdleten **Get-AzAppServicePlan** får en Azure App Service-plan i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="6fb02-108">The **Get-AzAppServicePlan** cmdlet gets an Azure App Service plan in the specified resource group.</span></span>

## <span data-ttu-id="6fb02-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6fb02-109">EXAMPLES</span></span>

### <span data-ttu-id="6fb02-110">Exempel 1: skaffa en app service-plan från en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="6fb02-110">Example 1: Get an App Service plan from a resource group</span></span>
```
PS C:\>Get-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="6fb02-111">Det här kommandot får App Service-planen med namnet ContosoASP som tillhör resurs gruppen som heter default-West-väst.</span><span class="sxs-lookup"><span data-stu-id="6fb02-111">This command gets the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

### <span data-ttu-id="6fb02-112">Exempel 2: skaffa alla program tjänst planer på en plats</span><span class="sxs-lookup"><span data-stu-id="6fb02-112">Example 2: Get all App Service plans in a location</span></span>
```
PS C:\>Get-AzAppServicePlan -Location "West US"
```

<span data-ttu-id="6fb02-113">Det här kommandot får alla App Service-abonnemang i "västra USA"-området.</span><span class="sxs-lookup"><span data-stu-id="6fb02-113">This command gets all App Service plans located in the "West US" region.</span></span>

## <span data-ttu-id="6fb02-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6fb02-114">PARAMETERS</span></span>

### <span data-ttu-id="6fb02-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fb02-115">-DefaultProfile</span></span>
<span data-ttu-id="6fb02-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6fb02-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6fb02-117">-Plats</span><span class="sxs-lookup"><span data-stu-id="6fb02-117">-Location</span></span>
<span data-ttu-id="6fb02-118">Plats</span><span class="sxs-lookup"><span data-stu-id="6fb02-118">Location</span></span> 

```yaml
Type: System.String
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fb02-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="6fb02-119">-Name</span></span>
<span data-ttu-id="6fb02-120">Namn på App Service-abonnemang</span><span class="sxs-lookup"><span data-stu-id="6fb02-120">App Service Plan Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fb02-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fb02-121">-ResourceGroupName</span></span>
<span data-ttu-id="6fb02-122">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="6fb02-122">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fb02-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fb02-123">CommonParameters</span></span>
<span data-ttu-id="6fb02-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6fb02-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fb02-125">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6fb02-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fb02-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6fb02-126">INPUTS</span></span>

### <span data-ttu-id="6fb02-127">Ingen</span><span class="sxs-lookup"><span data-stu-id="6fb02-127">None</span></span>

## <span data-ttu-id="6fb02-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6fb02-128">OUTPUTS</span></span>

### <span data-ttu-id="6fb02-129">Microsoft. Azure. commands. webapps. Models. WebApp. PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="6fb02-129">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="6fb02-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6fb02-130">NOTES</span></span>

## <span data-ttu-id="6fb02-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6fb02-131">RELATED LINKS</span></span>

[<span data-ttu-id="6fb02-132">New-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="6fb02-132">New-AzAppServicePlan</span></span>](./New-AzAppServicePlan.md)

[<span data-ttu-id="6fb02-133">Remove-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="6fb02-133">Remove-AzAppServicePlan</span></span>](./Remove-AzAppServicePlan.md)

[<span data-ttu-id="6fb02-134">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="6fb02-134">Set-AzAppServicePlan</span></span>](./Set-AzAppServicePlan.md)

