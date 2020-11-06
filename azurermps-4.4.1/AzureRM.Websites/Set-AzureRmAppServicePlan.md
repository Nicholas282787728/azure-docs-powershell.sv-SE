---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 32D45795-FBCD-4157-BF45-41BD1F61782E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmAppServicePlan.md
ms.openlocfilehash: 4b6270a6d56b8f210b2f03311bf19bb09950f361
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574963"
---
# <span data-ttu-id="96eb2-101">Set-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="96eb2-101">Set-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="96eb2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="96eb2-102">SYNOPSIS</span></span>
<span data-ttu-id="96eb2-103">Ställer in en Azure App Service-plan.</span><span class="sxs-lookup"><span data-stu-id="96eb2-103">Sets an Azure App Service plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="96eb2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="96eb2-104">SYNTAX</span></span>

### <span data-ttu-id="96eb2-105">S</span><span class="sxs-lookup"><span data-stu-id="96eb2-105">S1</span></span>
```
Set-AzureRmAppServicePlan [[-AdminSiteName] <String>] [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [-PerSiteScaling <Boolean>] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="96eb2-106">S2</span><span class="sxs-lookup"><span data-stu-id="96eb2-106">S2</span></span>
```
Set-AzureRmAppServicePlan [-AppServicePlan] <ServerFarmWithRichSku> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="96eb2-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="96eb2-107">DESCRIPTION</span></span>
<span data-ttu-id="96eb2-108">Cmdleten **set-AzureRmAppServicePlan** anger en Azure App Service-plan.</span><span class="sxs-lookup"><span data-stu-id="96eb2-108">The **Set-AzureRmAppServicePlan** cmdlet sets an Azure App Service plan.</span></span>

## <span data-ttu-id="96eb2-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="96eb2-109">EXAMPLES</span></span>

### <span data-ttu-id="96eb2-110">1: ändra en app service-plan</span><span class="sxs-lookup"><span data-stu-id="96eb2-110">1: Modify an App Service plan</span></span>
```
PS C:\>Set-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -PerSiteScaling $true
```

<span data-ttu-id="96eb2-111">Det här kommandot anger alternativet PerSiteScaling till true i App Service-planen med namnet ContosoASP som tillhör resurs gruppen med namnet default-Web-West.</span><span class="sxs-lookup"><span data-stu-id="96eb2-111">This command sets the PerSiteScaling option to true on the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="96eb2-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="96eb2-112">PARAMETERS</span></span>

### <span data-ttu-id="96eb2-113">-AdminSiteName</span><span class="sxs-lookup"><span data-stu-id="96eb2-113">-AdminSiteName</span></span>
<span data-ttu-id="96eb2-114">Namn på administratörs webbplats</span><span class="sxs-lookup"><span data-stu-id="96eb2-114">Admin Site Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96eb2-115">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="96eb2-115">-AppServicePlan</span></span>
<span data-ttu-id="96eb2-116">App Service plan-objekt</span><span class="sxs-lookup"><span data-stu-id="96eb2-116">App Service Plan Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="96eb2-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="96eb2-117">-Name</span></span>
<span data-ttu-id="96eb2-118">Namn på App Service-abonnemang</span><span class="sxs-lookup"><span data-stu-id="96eb2-118">App Service Plan Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96eb2-119">-NumberofWorkers</span><span class="sxs-lookup"><span data-stu-id="96eb2-119">-NumberofWorkers</span></span>
<span data-ttu-id="96eb2-120">Antal arbetare</span><span class="sxs-lookup"><span data-stu-id="96eb2-120">Number Of Workers</span></span>

```yaml
Type: System.Int32
Parameter Sets: S1
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96eb2-121">-PerSiteScaling</span><span class="sxs-lookup"><span data-stu-id="96eb2-121">-PerSiteScaling</span></span>
<span data-ttu-id="96eb2-122">Skalning för varje webbplats</span><span class="sxs-lookup"><span data-stu-id="96eb2-122">Per Site Scaling Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96eb2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96eb2-123">-ResourceGroupName</span></span>
<span data-ttu-id="96eb2-124">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="96eb2-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96eb2-125">-Tier</span><span class="sxs-lookup"><span data-stu-id="96eb2-125">-Tier</span></span>
<span data-ttu-id="96eb2-126">Sker</span><span class="sxs-lookup"><span data-stu-id="96eb2-126">Tier</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 
Accepted values: Free, Shared, Basic, Standard, Premium

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96eb2-127">-WorkerSize</span><span class="sxs-lookup"><span data-stu-id="96eb2-127">-WorkerSize</span></span>
<span data-ttu-id="96eb2-128">Arbetarens storlek</span><span class="sxs-lookup"><span data-stu-id="96eb2-128">Worker Size</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 
Accepted values: Small, Medium, Large, ExtraLarge

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96eb2-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96eb2-129">-DefaultProfile</span></span>
<span data-ttu-id="96eb2-130">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="96eb2-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="96eb2-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96eb2-131">CommonParameters</span></span>
<span data-ttu-id="96eb2-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96eb2-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96eb2-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96eb2-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96eb2-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="96eb2-134">INPUTS</span></span>

### <span data-ttu-id="96eb2-135">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="96eb2-135">ServerFarmWithRichSku</span></span>
<span data-ttu-id="96eb2-136">Parametern ' AppServicePlan ' godkänner värdet av typen ' ServerFarmWithRichSku ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="96eb2-136">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="96eb2-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="96eb2-137">OUTPUTS</span></span>

### <span data-ttu-id="96eb2-138">Microsoft. Azure. Management. webbplatser. Models. ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="96eb2-138">Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku</span></span>

## <span data-ttu-id="96eb2-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="96eb2-139">NOTES</span></span>

## <span data-ttu-id="96eb2-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="96eb2-140">RELATED LINKS</span></span>

[<span data-ttu-id="96eb2-141">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="96eb2-141">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="96eb2-142">New-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="96eb2-142">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="96eb2-143">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="96eb2-143">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="96eb2-144">Restart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="96eb2-144">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="96eb2-145">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="96eb2-145">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="96eb2-146">Stopp-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="96eb2-146">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


