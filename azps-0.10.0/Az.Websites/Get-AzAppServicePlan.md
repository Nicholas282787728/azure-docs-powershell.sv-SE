---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 89ED4231-7616-47D0-BDAA-D849C245DC79
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzAppServicePlan.md
ms.openlocfilehash: 48d37bf19ec6613ce1f42ee8cf7609bd6383e12f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923390"
---
# <span data-ttu-id="84da5-101">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="84da5-101">Get-AzAppServicePlan</span></span>

## <span data-ttu-id="84da5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="84da5-102">SYNOPSIS</span></span>
<span data-ttu-id="84da5-103">Hämtar en Azure App Service-plan i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="84da5-103">Gets an Azure App Service plan in the specified resource group.</span></span>

## <span data-ttu-id="84da5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="84da5-104">SYNTAX</span></span>

### <span data-ttu-id="84da5-105">S</span><span class="sxs-lookup"><span data-stu-id="84da5-105">S1</span></span>
```
Get-AzAppServicePlan [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="84da5-106">S2</span><span class="sxs-lookup"><span data-stu-id="84da5-106">S2</span></span>
```
Get-AzAppServicePlan [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="84da5-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="84da5-107">DESCRIPTION</span></span>
<span data-ttu-id="84da5-108">Cmdleten **Get-AzAppServicePlan** får en Azure App Service-plan i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="84da5-108">The **Get-AzAppServicePlan** cmdlet gets an Azure App Service plan in the specified resource group.</span></span>

## <span data-ttu-id="84da5-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="84da5-109">EXAMPLES</span></span>

### <span data-ttu-id="84da5-110">Exempel 1: skaffa en app service-plan från en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="84da5-110">Example 1: Get an App Service plan from a resource group</span></span>
```
PS C:\>Get-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="84da5-111">Det här kommandot får App Service-planen med namnet ContosoASP som tillhör resurs gruppen som heter default-West-väst.</span><span class="sxs-lookup"><span data-stu-id="84da5-111">This command gets the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

### <span data-ttu-id="84da5-112">Exempel 2: skaffa alla program tjänst planer på en plats</span><span class="sxs-lookup"><span data-stu-id="84da5-112">Example 2: Get all App Service plans in a location</span></span>
```
PS C:\>Get-AzAppServicePlan -Location "West US"
```

<span data-ttu-id="84da5-113">Det här kommandot får alla App Service-abonnemang i "västra USA"-området.</span><span class="sxs-lookup"><span data-stu-id="84da5-113">This command gets all App Service plans located in the "West US" region.</span></span>

## <span data-ttu-id="84da5-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="84da5-114">PARAMETERS</span></span>

### <span data-ttu-id="84da5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84da5-115">-DefaultProfile</span></span>
<span data-ttu-id="84da5-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="84da5-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="84da5-117">-Plats</span><span class="sxs-lookup"><span data-stu-id="84da5-117">-Location</span></span>
<span data-ttu-id="84da5-118">Plats</span><span class="sxs-lookup"><span data-stu-id="84da5-118">Location</span></span> 

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

### <span data-ttu-id="84da5-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="84da5-119">-Name</span></span>
<span data-ttu-id="84da5-120">Namn på App Service-abonnemang</span><span class="sxs-lookup"><span data-stu-id="84da5-120">App Service Plan Name</span></span>

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

### <span data-ttu-id="84da5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84da5-121">-ResourceGroupName</span></span>
<span data-ttu-id="84da5-122">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="84da5-122">Resource Group Name</span></span>

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

### <span data-ttu-id="84da5-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84da5-123">CommonParameters</span></span>
<span data-ttu-id="84da5-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84da5-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84da5-125">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84da5-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84da5-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="84da5-126">INPUTS</span></span>

### <span data-ttu-id="84da5-127">Ingen</span><span class="sxs-lookup"><span data-stu-id="84da5-127">None</span></span>
<span data-ttu-id="84da5-128">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="84da5-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="84da5-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="84da5-129">OUTPUTS</span></span>

### <span data-ttu-id="84da5-130">Microsoft. Azure. Management. webbplatser. Models. ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="84da5-130">Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku</span></span>

### <span data-ttu-id="84da5-131">Microsoft. Azure. Management. webbplatser. Models. ServerFarmCollection</span><span class="sxs-lookup"><span data-stu-id="84da5-131">Microsoft.Azure.Management.WebSites.Models.ServerFarmCollection</span></span>

## <span data-ttu-id="84da5-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="84da5-132">NOTES</span></span>

## <span data-ttu-id="84da5-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="84da5-133">RELATED LINKS</span></span>

[<span data-ttu-id="84da5-134">New-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="84da5-134">New-AzAppServicePlan</span></span>](./New-AzAppServicePlan.md)

[<span data-ttu-id="84da5-135">Remove-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="84da5-135">Remove-AzAppServicePlan</span></span>](./Remove-AzAppServicePlan.md)

[<span data-ttu-id="84da5-136">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="84da5-136">Set-AzAppServicePlan</span></span>](./Set-AzAppServicePlan.md)


