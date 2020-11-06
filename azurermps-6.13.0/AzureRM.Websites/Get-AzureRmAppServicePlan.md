---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 89ED4231-7616-47D0-BDAA-D849C245DC79
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmAppServicePlan.md
ms.openlocfilehash: 9fe7d3d9580411c31fdf5ca7e21ba1c4379217a4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577772"
---
# <span data-ttu-id="9e0d0-101">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="9e0d0-101">Get-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="9e0d0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9e0d0-102">SYNOPSIS</span></span>
<span data-ttu-id="9e0d0-103">Hämtar en Azure App Service-plan i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="9e0d0-103">Gets an Azure App Service plan in the specified resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9e0d0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9e0d0-104">SYNTAX</span></span>

### <span data-ttu-id="9e0d0-105">S</span><span class="sxs-lookup"><span data-stu-id="9e0d0-105">S1</span></span>
```
Get-AzureRmAppServicePlan [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e0d0-106">S2</span><span class="sxs-lookup"><span data-stu-id="9e0d0-106">S2</span></span>
```
Get-AzureRmAppServicePlan [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e0d0-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9e0d0-107">DESCRIPTION</span></span>
<span data-ttu-id="9e0d0-108">Cmdleten **Get-AzureRmAppServicePlan** får en Azure App Service-plan i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="9e0d0-108">The **Get-AzureRmAppServicePlan** cmdlet gets an Azure App Service plan in the specified resource group.</span></span>

## <span data-ttu-id="9e0d0-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9e0d0-109">EXAMPLES</span></span>

### <span data-ttu-id="9e0d0-110">Exempel 1: skaffa en app service-plan från en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="9e0d0-110">Example 1: Get an App Service plan from a resource group</span></span>
```
PS C:\>Get-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="9e0d0-111">Det här kommandot får App Service-planen med namnet ContosoASP som tillhör resurs gruppen som heter default-West-väst.</span><span class="sxs-lookup"><span data-stu-id="9e0d0-111">This command gets the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

### <span data-ttu-id="9e0d0-112">Exempel 2: skaffa alla program tjänst planer på en plats</span><span class="sxs-lookup"><span data-stu-id="9e0d0-112">Example 2: Get all App Service plans in a location</span></span>
```
PS C:\>Get-AzureRmAppServicePlan -Location "West US"
```

<span data-ttu-id="9e0d0-113">Det här kommandot får alla App Service-abonnemang i "västra USA"-området.</span><span class="sxs-lookup"><span data-stu-id="9e0d0-113">This command gets all App Service plans located in the "West US" region.</span></span>

## <span data-ttu-id="9e0d0-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9e0d0-114">PARAMETERS</span></span>

### <span data-ttu-id="9e0d0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e0d0-115">-DefaultProfile</span></span>
<span data-ttu-id="9e0d0-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9e0d0-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9e0d0-117">-Plats</span><span class="sxs-lookup"><span data-stu-id="9e0d0-117">-Location</span></span>
<span data-ttu-id="9e0d0-118">Plats</span><span class="sxs-lookup"><span data-stu-id="9e0d0-118">Location</span></span> 

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

### <span data-ttu-id="9e0d0-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="9e0d0-119">-Name</span></span>
<span data-ttu-id="9e0d0-120">Namn på App Service-abonnemang</span><span class="sxs-lookup"><span data-stu-id="9e0d0-120">App Service Plan Name</span></span>

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

### <span data-ttu-id="9e0d0-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e0d0-121">-ResourceGroupName</span></span>
<span data-ttu-id="9e0d0-122">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="9e0d0-122">Resource Group Name</span></span>

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

### <span data-ttu-id="9e0d0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e0d0-123">CommonParameters</span></span>
<span data-ttu-id="9e0d0-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e0d0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e0d0-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e0d0-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e0d0-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9e0d0-126">INPUTS</span></span>

### <span data-ttu-id="9e0d0-127">Ingen</span><span class="sxs-lookup"><span data-stu-id="9e0d0-127">None</span></span>

## <span data-ttu-id="9e0d0-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9e0d0-128">OUTPUTS</span></span>

### <span data-ttu-id="9e0d0-129">Microsoft. Azure. Management. webbplatser. Models. AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="9e0d0-129">Microsoft.Azure.Management.WebSites.Models.AppServicePlan</span></span>

## <span data-ttu-id="9e0d0-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9e0d0-130">NOTES</span></span>

## <span data-ttu-id="9e0d0-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9e0d0-131">RELATED LINKS</span></span>

[<span data-ttu-id="9e0d0-132">New-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="9e0d0-132">New-AzureRmAppServicePlan</span></span>](./New-AzureRmAppServicePlan.md)

[<span data-ttu-id="9e0d0-133">Remove-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="9e0d0-133">Remove-AzureRmAppServicePlan</span></span>](./Remove-AzureRmAppServicePlan.md)

[<span data-ttu-id="9e0d0-134">Set-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="9e0d0-134">Set-AzureRmAppServicePlan</span></span>](./Set-AzureRmAppServicePlan.md)


