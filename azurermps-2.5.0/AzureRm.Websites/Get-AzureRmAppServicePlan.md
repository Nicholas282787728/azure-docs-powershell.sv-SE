---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 89ED4231-7616-47D0-BDAA-D849C245DC79
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermappserviceplan
schema: 2.0.0
ms.openlocfilehash: b85d22d1030eaa12e58cded1c7225231c7e8b964
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929201"
---
# <span data-ttu-id="eacc3-101">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="eacc3-101">Get-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="eacc3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="eacc3-102">SYNOPSIS</span></span>
<span data-ttu-id="eacc3-103">Hämtar en Azure App Service-plan i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="eacc3-103">Gets an Azure App Service plan in the specified resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eacc3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="eacc3-104">SYNTAX</span></span>

### <span data-ttu-id="eacc3-105">S</span><span class="sxs-lookup"><span data-stu-id="eacc3-105">S1</span></span>
```
Get-AzureRmAppServicePlan [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eacc3-106">S2</span><span class="sxs-lookup"><span data-stu-id="eacc3-106">S2</span></span>
```
Get-AzureRmAppServicePlan [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eacc3-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="eacc3-107">DESCRIPTION</span></span>
<span data-ttu-id="eacc3-108">Cmdleten **Get-AzureRmAppServicePlan** får en Azure App Service-plan i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="eacc3-108">The **Get-AzureRmAppServicePlan** cmdlet gets an Azure App Service plan in the specified resource group.</span></span>

## <span data-ttu-id="eacc3-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="eacc3-109">EXAMPLES</span></span>

### <span data-ttu-id="eacc3-110">Exempel 1: skaffa en app service-plan från en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="eacc3-110">Example 1: Get an App Service plan from a resource group</span></span>
```
PS C:\>Get-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="eacc3-111">Det här kommandot får App Service-planen med namnet ContosoASP som tillhör resurs gruppen som heter default-West-väst.</span><span class="sxs-lookup"><span data-stu-id="eacc3-111">This command gets the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

### <span data-ttu-id="eacc3-112">Exempel 2: skaffa alla program tjänst planer på en plats</span><span class="sxs-lookup"><span data-stu-id="eacc3-112">Example 2: Get all App Service plans in a location</span></span>
```
PS C:\>Get-AzureRmAppServicePlan -Location "West US"
```

<span data-ttu-id="eacc3-113">Det här kommandot får alla App Service-abonnemang i "västra USA"-området.</span><span class="sxs-lookup"><span data-stu-id="eacc3-113">This command gets all App Service plans located in the "West US" region.</span></span>

## <span data-ttu-id="eacc3-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="eacc3-114">PARAMETERS</span></span>

### <span data-ttu-id="eacc3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eacc3-115">-DefaultProfile</span></span>
<span data-ttu-id="eacc3-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="eacc3-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eacc3-117">-Plats</span><span class="sxs-lookup"><span data-stu-id="eacc3-117">-Location</span></span>
<span data-ttu-id="eacc3-118">Plats</span><span class="sxs-lookup"><span data-stu-id="eacc3-118">Location</span></span> 

```yaml
Type: String
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eacc3-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="eacc3-119">-Name</span></span>
<span data-ttu-id="eacc3-120">Namn på App Service-abonnemang</span><span class="sxs-lookup"><span data-stu-id="eacc3-120">App Service Plan Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eacc3-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eacc3-121">-ResourceGroupName</span></span>
<span data-ttu-id="eacc3-122">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="eacc3-122">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eacc3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eacc3-123">CommonParameters</span></span>
<span data-ttu-id="eacc3-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eacc3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eacc3-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eacc3-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eacc3-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="eacc3-126">INPUTS</span></span>

### <span data-ttu-id="eacc3-127">Ingen</span><span class="sxs-lookup"><span data-stu-id="eacc3-127">None</span></span>
<span data-ttu-id="eacc3-128">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="eacc3-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="eacc3-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="eacc3-129">OUTPUTS</span></span>

### <span data-ttu-id="eacc3-130">Microsoft. Azure. Management. webbplatser. Models. ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="eacc3-130">Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku</span></span>

### <span data-ttu-id="eacc3-131">Microsoft. Azure. Management. webbplatser. Models. ServerFarmCollection</span><span class="sxs-lookup"><span data-stu-id="eacc3-131">Microsoft.Azure.Management.WebSites.Models.ServerFarmCollection</span></span>

## <span data-ttu-id="eacc3-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="eacc3-132">NOTES</span></span>

## <span data-ttu-id="eacc3-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="eacc3-133">RELATED LINKS</span></span>

[<span data-ttu-id="eacc3-134">New-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="eacc3-134">New-AzureRmAppServicePlan</span></span>](./New-AzureRmAppServicePlan.md)

[<span data-ttu-id="eacc3-135">Remove-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="eacc3-135">Remove-AzureRmAppServicePlan</span></span>](./Remove-AzureRmAppServicePlan.md)

[<span data-ttu-id="eacc3-136">Set-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="eacc3-136">Set-AzureRmAppServicePlan</span></span>](./Set-AzureRmAppServicePlan.md)


