---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 32D45795-FBCD-4157-BF45-41BD1F61782E
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzAppServicePlan.md
ms.openlocfilehash: d27dc8ae315eb587ccb129125500a86e22429773
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746025"
---
# <span data-ttu-id="073ea-101">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="073ea-101">Set-AzAppServicePlan</span></span>

## <span data-ttu-id="073ea-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="073ea-102">SYNOPSIS</span></span>
<span data-ttu-id="073ea-103">Ställer in en Azure App Service-plan.</span><span class="sxs-lookup"><span data-stu-id="073ea-103">Sets an Azure App Service plan.</span></span>

## <span data-ttu-id="073ea-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="073ea-104">SYNTAX</span></span>

### <span data-ttu-id="073ea-105">S</span><span class="sxs-lookup"><span data-stu-id="073ea-105">S1</span></span>
```
Set-AzAppServicePlan [[-AdminSiteName] <String>] [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [-PerSiteScaling <Boolean>] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="073ea-106">S2</span><span class="sxs-lookup"><span data-stu-id="073ea-106">S2</span></span>
```
Set-AzAppServicePlan [-AsJob] [-AppServicePlan] <PSAppServicePlan> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="073ea-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="073ea-107">DESCRIPTION</span></span>
<span data-ttu-id="073ea-108">Cmdleten **set-AzAppServicePlan** anger en Azure App Service-plan.</span><span class="sxs-lookup"><span data-stu-id="073ea-108">The **Set-AzAppServicePlan** cmdlet sets an Azure App Service plan.</span></span>

## <span data-ttu-id="073ea-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="073ea-109">EXAMPLES</span></span>

### <span data-ttu-id="073ea-110">1: ändra en app service-plan</span><span class="sxs-lookup"><span data-stu-id="073ea-110">1: Modify an App Service plan</span></span>
```
PS C:\>Set-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -PerSiteScaling $true
```

<span data-ttu-id="073ea-111">Det här kommandot anger alternativet PerSiteScaling till true i App Service-planen med namnet ContosoASP som tillhör resurs gruppen med namnet default-Web-West.</span><span class="sxs-lookup"><span data-stu-id="073ea-111">This command sets the PerSiteScaling option to true on the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="073ea-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="073ea-112">PARAMETERS</span></span>

### <span data-ttu-id="073ea-113">-AdminSiteName</span><span class="sxs-lookup"><span data-stu-id="073ea-113">-AdminSiteName</span></span>
<span data-ttu-id="073ea-114">Namn på administratörs webbplats</span><span class="sxs-lookup"><span data-stu-id="073ea-114">Admin Site Name</span></span>

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

### <span data-ttu-id="073ea-115">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="073ea-115">-AppServicePlan</span></span>
<span data-ttu-id="073ea-116">App Service plan-objekt</span><span class="sxs-lookup"><span data-stu-id="073ea-116">App Service Plan Object</span></span>

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

### <span data-ttu-id="073ea-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="073ea-117">-AsJob</span></span>
<span data-ttu-id="073ea-118">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="073ea-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="073ea-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="073ea-119">-DefaultProfile</span></span>
<span data-ttu-id="073ea-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="073ea-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="073ea-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="073ea-121">-Name</span></span>
<span data-ttu-id="073ea-122">Namn på App Service-abonnemang</span><span class="sxs-lookup"><span data-stu-id="073ea-122">App Service Plan Name</span></span>

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

### <span data-ttu-id="073ea-123">-NumberofWorkers</span><span class="sxs-lookup"><span data-stu-id="073ea-123">-NumberofWorkers</span></span>
<span data-ttu-id="073ea-124">Antal arbetare</span><span class="sxs-lookup"><span data-stu-id="073ea-124">Number Of Workers</span></span>

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

### <span data-ttu-id="073ea-125">-PerSiteScaling</span><span class="sxs-lookup"><span data-stu-id="073ea-125">-PerSiteScaling</span></span>
<span data-ttu-id="073ea-126">Skalning för varje webbplats</span><span class="sxs-lookup"><span data-stu-id="073ea-126">Per Site Scaling Boolean</span></span>

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

### <span data-ttu-id="073ea-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="073ea-127">-ResourceGroupName</span></span>
<span data-ttu-id="073ea-128">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="073ea-128">Resource Group Name</span></span>

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

### <span data-ttu-id="073ea-129">-Tier</span><span class="sxs-lookup"><span data-stu-id="073ea-129">-Tier</span></span>
<span data-ttu-id="073ea-130">Sker</span><span class="sxs-lookup"><span data-stu-id="073ea-130">Tier</span></span>

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

### <span data-ttu-id="073ea-131">-WorkerSize</span><span class="sxs-lookup"><span data-stu-id="073ea-131">-WorkerSize</span></span>
<span data-ttu-id="073ea-132">Arbetarens storlek</span><span class="sxs-lookup"><span data-stu-id="073ea-132">Worker Size</span></span>

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

### <span data-ttu-id="073ea-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="073ea-133">CommonParameters</span></span>
<span data-ttu-id="073ea-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="073ea-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="073ea-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="073ea-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="073ea-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="073ea-136">INPUTS</span></span>

### <span data-ttu-id="073ea-137">Microsoft. Azure. commands. webapps. Models. WebApp. PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="073ea-137">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="073ea-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="073ea-138">OUTPUTS</span></span>

### <span data-ttu-id="073ea-139">Microsoft. Azure. commands. webapps. Models. WebApp. PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="073ea-139">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="073ea-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="073ea-140">NOTES</span></span>

## <span data-ttu-id="073ea-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="073ea-141">RELATED LINKS</span></span>

[<span data-ttu-id="073ea-142">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="073ea-142">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="073ea-143">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="073ea-143">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="073ea-144">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="073ea-144">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="073ea-145">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="073ea-145">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="073ea-146">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="073ea-146">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="073ea-147">Stopp-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="073ea-147">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


