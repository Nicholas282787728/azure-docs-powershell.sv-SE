---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 89ED4231-7616-47D0-BDAA-D849C245DC79
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmAppServicePlan.md
ms.openlocfilehash: 9cadc32a34f94a29221984e25141bcc3a844de4d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756309"
---
# <span data-ttu-id="c501b-101">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="c501b-101">Get-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="c501b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c501b-102">SYNOPSIS</span></span>
<span data-ttu-id="c501b-103">Hämtar en Azure App Service-plan i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="c501b-103">Gets an Azure App Service plan in the specified resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c501b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c501b-104">SYNTAX</span></span>

### <span data-ttu-id="c501b-105">S</span><span class="sxs-lookup"><span data-stu-id="c501b-105">S1</span></span>
```
Get-AzureRmAppServicePlan [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c501b-106">S2</span><span class="sxs-lookup"><span data-stu-id="c501b-106">S2</span></span>
```
Get-AzureRmAppServicePlan [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c501b-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c501b-107">DESCRIPTION</span></span>
<span data-ttu-id="c501b-108">Cmdleten **Get-AzureRmAppServicePlan** får en Azure App Service-plan i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="c501b-108">The **Get-AzureRmAppServicePlan** cmdlet gets an Azure App Service plan in the specified resource group.</span></span>

## <span data-ttu-id="c501b-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c501b-109">EXAMPLES</span></span>

### <span data-ttu-id="c501b-110">Exempel 1: skaffa en app service-plan från en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="c501b-110">Example 1: Get an App Service plan from a resource group</span></span>
```
PS C:\>Get-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="c501b-111">Det här kommandot får App Service-planen med namnet ContosoASP som tillhör resurs gruppen som heter default-West-väst.</span><span class="sxs-lookup"><span data-stu-id="c501b-111">This command gets the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

### <span data-ttu-id="c501b-112">Exempel 2: skaffa alla program tjänst planer på en plats</span><span class="sxs-lookup"><span data-stu-id="c501b-112">Example 2: Get all App Service plans in a location</span></span>
```
PS C:\>Get-AzureRmAppServicePlan -Location "West US"
```

<span data-ttu-id="c501b-113">Det här kommandot får alla App Service-abonnemang i "västra USA"-området.</span><span class="sxs-lookup"><span data-stu-id="c501b-113">This command gets all App Service plans located in the "West US" region.</span></span>

## <span data-ttu-id="c501b-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c501b-114">PARAMETERS</span></span>

### <span data-ttu-id="c501b-115">-Plats</span><span class="sxs-lookup"><span data-stu-id="c501b-115">-Location</span></span>
<span data-ttu-id="c501b-116">Plats</span><span class="sxs-lookup"><span data-stu-id="c501b-116">Location</span></span> 

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

### <span data-ttu-id="c501b-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="c501b-117">-Name</span></span>
<span data-ttu-id="c501b-118">Namn på App Service-abonnemang</span><span class="sxs-lookup"><span data-stu-id="c501b-118">App Service Plan Name</span></span>

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

### <span data-ttu-id="c501b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c501b-119">-ResourceGroupName</span></span>
<span data-ttu-id="c501b-120">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="c501b-120">Resource Group Name</span></span>

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

### <span data-ttu-id="c501b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c501b-121">-DefaultProfile</span></span>
<span data-ttu-id="c501b-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c501b-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c501b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c501b-123">CommonParameters</span></span>
<span data-ttu-id="c501b-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c501b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c501b-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c501b-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c501b-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c501b-126">INPUTS</span></span>

## <span data-ttu-id="c501b-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c501b-127">OUTPUTS</span></span>

### <span data-ttu-id="c501b-128">Microsoft. Azure. Management. webbplatser. Models. ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="c501b-128">Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku</span></span>

### <span data-ttu-id="c501b-129">Microsoft. Azure. Management. webbplatser. Models. ServerFarmCollection</span><span class="sxs-lookup"><span data-stu-id="c501b-129">Microsoft.Azure.Management.WebSites.Models.ServerFarmCollection</span></span>

## <span data-ttu-id="c501b-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c501b-130">NOTES</span></span>

## <span data-ttu-id="c501b-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c501b-131">RELATED LINKS</span></span>

[<span data-ttu-id="c501b-132">New-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="c501b-132">New-AzureRmAppServicePlan</span></span>](./New-AzureRmAppServicePlan.md)

[<span data-ttu-id="c501b-133">Remove-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="c501b-133">Remove-AzureRmAppServicePlan</span></span>](./Remove-AzureRmAppServicePlan.md)

[<span data-ttu-id="c501b-134">Set-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="c501b-134">Set-AzureRmAppServicePlan</span></span>](./Set-AzureRmAppServicePlan.md)


