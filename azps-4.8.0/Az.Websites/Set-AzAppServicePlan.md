---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 32D45795-FBCD-4157-BF45-41BD1F61782E
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzAppServicePlan.md
ms.openlocfilehash: b56766908ba993ccff056ce10acc81bba7a7196f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94100666"
---
# <span data-ttu-id="a92b8-101">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="a92b8-101">Set-AzAppServicePlan</span></span>

## <span data-ttu-id="a92b8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a92b8-102">SYNOPSIS</span></span>
<span data-ttu-id="a92b8-103">Ställer in en Azure App Service-plan.</span><span class="sxs-lookup"><span data-stu-id="a92b8-103">Sets an Azure App Service plan.</span></span>

## <span data-ttu-id="a92b8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a92b8-104">SYNTAX</span></span>

### <span data-ttu-id="a92b8-105">S</span><span class="sxs-lookup"><span data-stu-id="a92b8-105">S1</span></span>
```
Set-AzAppServicePlan [[-AdminSiteName] <String>] [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [-PerSiteScaling <Boolean>] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a92b8-106">S2</span><span class="sxs-lookup"><span data-stu-id="a92b8-106">S2</span></span>
```
Set-AzAppServicePlan [-AsJob] [-AppServicePlan] <PSAppServicePlan> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a92b8-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a92b8-107">DESCRIPTION</span></span>
<span data-ttu-id="a92b8-108">Cmdleten **set-AzAppServicePlan** anger en Azure App Service-plan.</span><span class="sxs-lookup"><span data-stu-id="a92b8-108">The **Set-AzAppServicePlan** cmdlet sets an Azure App Service plan.</span></span>

## <span data-ttu-id="a92b8-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a92b8-109">EXAMPLES</span></span>

### <span data-ttu-id="a92b8-110">Exempel 1: ändra en app service-plan</span><span class="sxs-lookup"><span data-stu-id="a92b8-110">Example 1: Modify an App Service plan</span></span>
```powershell
PS C:\>Set-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -PerSiteScaling $true
```

<span data-ttu-id="a92b8-111">Det här kommandot anger alternativet PerSiteScaling till true i App Service-planen med namnet ContosoASP som tillhör resurs gruppen med namnet default-Web-West.</span><span class="sxs-lookup"><span data-stu-id="a92b8-111">This command sets the PerSiteScaling option to true on the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

### <span data-ttu-id="a92b8-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="a92b8-112">Example 2</span></span>

<span data-ttu-id="a92b8-113">Ställer in en Azure App Service-plan.</span><span class="sxs-lookup"><span data-stu-id="a92b8-113">Sets an Azure App Service plan.</span></span> <span data-ttu-id="a92b8-114">(automatiskt genererat)</span><span class="sxs-lookup"><span data-stu-id="a92b8-114">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzAppServicePlan -Name 'ContosoASP' -ResourceGroupName 'Default-Web-WestUS' -Tier Free -WorkerSize Small
```

## <span data-ttu-id="a92b8-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a92b8-115">PARAMETERS</span></span>

### <span data-ttu-id="a92b8-116">-AdminSiteName</span><span class="sxs-lookup"><span data-stu-id="a92b8-116">-AdminSiteName</span></span>
<span data-ttu-id="a92b8-117">Namn på administratörs webbplats</span><span class="sxs-lookup"><span data-stu-id="a92b8-117">Admin Site Name</span></span>

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

### <span data-ttu-id="a92b8-118">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="a92b8-118">-AppServicePlan</span></span>
<span data-ttu-id="a92b8-119">App Service plan-objekt</span><span class="sxs-lookup"><span data-stu-id="a92b8-119">App Service Plan Object</span></span>

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

### <span data-ttu-id="a92b8-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a92b8-120">-AsJob</span></span>
<span data-ttu-id="a92b8-121">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="a92b8-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a92b8-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a92b8-122">-DefaultProfile</span></span>
<span data-ttu-id="a92b8-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a92b8-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a92b8-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="a92b8-124">-Name</span></span>
<span data-ttu-id="a92b8-125">Namn på App Service-abonnemang</span><span class="sxs-lookup"><span data-stu-id="a92b8-125">App Service Plan Name</span></span>

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

### <span data-ttu-id="a92b8-126">-NumberofWorkers</span><span class="sxs-lookup"><span data-stu-id="a92b8-126">-NumberofWorkers</span></span>
<span data-ttu-id="a92b8-127">Antal arbetare</span><span class="sxs-lookup"><span data-stu-id="a92b8-127">Number Of Workers</span></span>

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

### <span data-ttu-id="a92b8-128">-PerSiteScaling</span><span class="sxs-lookup"><span data-stu-id="a92b8-128">-PerSiteScaling</span></span>
<span data-ttu-id="a92b8-129">Skalning för varje webbplats</span><span class="sxs-lookup"><span data-stu-id="a92b8-129">Per Site Scaling Boolean</span></span>

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

### <span data-ttu-id="a92b8-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a92b8-130">-ResourceGroupName</span></span>
<span data-ttu-id="a92b8-131">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="a92b8-131">Resource Group Name</span></span>

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

### <span data-ttu-id="a92b8-132">-Tier</span><span class="sxs-lookup"><span data-stu-id="a92b8-132">-Tier</span></span>
<span data-ttu-id="a92b8-133">Sker</span><span class="sxs-lookup"><span data-stu-id="a92b8-133">Tier</span></span>

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

### <span data-ttu-id="a92b8-134">-WorkerSize</span><span class="sxs-lookup"><span data-stu-id="a92b8-134">-WorkerSize</span></span>
<span data-ttu-id="a92b8-135">Arbetarens storlek</span><span class="sxs-lookup"><span data-stu-id="a92b8-135">Worker Size</span></span>

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

### <span data-ttu-id="a92b8-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a92b8-136">CommonParameters</span></span>
<span data-ttu-id="a92b8-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a92b8-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a92b8-138">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a92b8-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a92b8-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a92b8-139">INPUTS</span></span>

### <span data-ttu-id="a92b8-140">Microsoft. Azure. commands. webapps. Models. WebApp. PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="a92b8-140">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="a92b8-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a92b8-141">OUTPUTS</span></span>

### <span data-ttu-id="a92b8-142">Microsoft. Azure. commands. webapps. Models. WebApp. PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="a92b8-142">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="a92b8-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a92b8-143">NOTES</span></span>

## <span data-ttu-id="a92b8-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a92b8-144">RELATED LINKS</span></span>

[<span data-ttu-id="a92b8-145">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a92b8-145">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="a92b8-146">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a92b8-146">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="a92b8-147">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a92b8-147">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="a92b8-148">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a92b8-148">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="a92b8-149">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a92b8-149">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="a92b8-150">Stopp-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a92b8-150">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)

