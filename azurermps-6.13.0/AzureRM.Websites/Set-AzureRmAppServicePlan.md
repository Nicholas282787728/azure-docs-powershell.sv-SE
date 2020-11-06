---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 32D45795-FBCD-4157-BF45-41BD1F61782E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/set-azurermappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmAppServicePlan.md
ms.openlocfilehash: 2163c18fecadba069b7c3fba260ab81538ed5583
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577723"
---
# <span data-ttu-id="ec973-101">Set-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="ec973-101">Set-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="ec973-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ec973-102">SYNOPSIS</span></span>
<span data-ttu-id="ec973-103">Ställer in en Azure App Service-plan.</span><span class="sxs-lookup"><span data-stu-id="ec973-103">Sets an Azure App Service plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ec973-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ec973-104">SYNTAX</span></span>

### <span data-ttu-id="ec973-105">S</span><span class="sxs-lookup"><span data-stu-id="ec973-105">S1</span></span>
```
Set-AzureRmAppServicePlan [[-AdminSiteName] <String>] [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [-PerSiteScaling <Boolean>] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ec973-106">S2</span><span class="sxs-lookup"><span data-stu-id="ec973-106">S2</span></span>
```
Set-AzureRmAppServicePlan [-AsJob] [-AppServicePlan] <PSAppServicePlan>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ec973-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ec973-107">DESCRIPTION</span></span>
<span data-ttu-id="ec973-108">Cmdleten **set-AzureRmAppServicePlan** anger en Azure App Service-plan.</span><span class="sxs-lookup"><span data-stu-id="ec973-108">The **Set-AzureRmAppServicePlan** cmdlet sets an Azure App Service plan.</span></span>

## <span data-ttu-id="ec973-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ec973-109">EXAMPLES</span></span>

### <span data-ttu-id="ec973-110">1: ändra en app service-plan</span><span class="sxs-lookup"><span data-stu-id="ec973-110">1: Modify an App Service plan</span></span>
```
PS C:\>Set-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -PerSiteScaling $true
```

<span data-ttu-id="ec973-111">Det här kommandot anger alternativet PerSiteScaling till true i App Service-planen med namnet ContosoASP som tillhör resurs gruppen med namnet default-Web-West.</span><span class="sxs-lookup"><span data-stu-id="ec973-111">This command sets the PerSiteScaling option to true on the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="ec973-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ec973-112">PARAMETERS</span></span>

### <span data-ttu-id="ec973-113">-AdminSiteName</span><span class="sxs-lookup"><span data-stu-id="ec973-113">-AdminSiteName</span></span>
<span data-ttu-id="ec973-114">Namn på administratörs webbplats</span><span class="sxs-lookup"><span data-stu-id="ec973-114">Admin Site Name</span></span>

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

### <span data-ttu-id="ec973-115">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="ec973-115">-AppServicePlan</span></span>
<span data-ttu-id="ec973-116">App Service plan-objekt</span><span class="sxs-lookup"><span data-stu-id="ec973-116">App Service Plan Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ec973-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ec973-117">-AsJob</span></span>
<span data-ttu-id="ec973-118">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="ec973-118">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec973-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec973-119">-DefaultProfile</span></span>
<span data-ttu-id="ec973-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ec973-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ec973-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="ec973-121">-Name</span></span>
<span data-ttu-id="ec973-122">Namn på App Service-abonnemang</span><span class="sxs-lookup"><span data-stu-id="ec973-122">App Service Plan Name</span></span>

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

### <span data-ttu-id="ec973-123">-NumberofWorkers</span><span class="sxs-lookup"><span data-stu-id="ec973-123">-NumberofWorkers</span></span>
<span data-ttu-id="ec973-124">Antal arbetare</span><span class="sxs-lookup"><span data-stu-id="ec973-124">Number Of Workers</span></span>

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

### <span data-ttu-id="ec973-125">-PerSiteScaling</span><span class="sxs-lookup"><span data-stu-id="ec973-125">-PerSiteScaling</span></span>
<span data-ttu-id="ec973-126">Skalning för varje webbplats</span><span class="sxs-lookup"><span data-stu-id="ec973-126">Per Site Scaling Boolean</span></span>

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

### <span data-ttu-id="ec973-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec973-127">-ResourceGroupName</span></span>
<span data-ttu-id="ec973-128">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="ec973-128">Resource Group Name</span></span>

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

### <span data-ttu-id="ec973-129">-Tier</span><span class="sxs-lookup"><span data-stu-id="ec973-129">-Tier</span></span>
<span data-ttu-id="ec973-130">Sker</span><span class="sxs-lookup"><span data-stu-id="ec973-130">Tier</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec973-131">-WorkerSize</span><span class="sxs-lookup"><span data-stu-id="ec973-131">-WorkerSize</span></span>
<span data-ttu-id="ec973-132">Arbetarens storlek</span><span class="sxs-lookup"><span data-stu-id="ec973-132">Worker Size</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec973-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec973-133">CommonParameters</span></span>
<span data-ttu-id="ec973-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec973-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec973-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec973-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec973-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ec973-136">INPUTS</span></span>

### <span data-ttu-id="ec973-137">Microsoft. Azure. Management. webbplatser. Models. AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="ec973-137">Microsoft.Azure.Management.WebSites.Models.AppServicePlan</span></span>
<span data-ttu-id="ec973-138">Parametrar: AppServicePlan (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ec973-138">Parameters: AppServicePlan (ByValue)</span></span>

## <span data-ttu-id="ec973-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ec973-139">OUTPUTS</span></span>

### <span data-ttu-id="ec973-140">Microsoft. Azure. Management. webbplatser. Models. AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="ec973-140">Microsoft.Azure.Management.WebSites.Models.AppServicePlan</span></span>

## <span data-ttu-id="ec973-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ec973-141">NOTES</span></span>

## <span data-ttu-id="ec973-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ec973-142">RELATED LINKS</span></span>

[<span data-ttu-id="ec973-143">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="ec973-143">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="ec973-144">New-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="ec973-144">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="ec973-145">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="ec973-145">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="ec973-146">Restart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="ec973-146">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="ec973-147">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="ec973-147">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="ec973-148">Stopp-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="ec973-148">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


