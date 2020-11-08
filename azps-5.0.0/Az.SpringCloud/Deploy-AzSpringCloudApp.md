---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.SpringCloud/deploy-azSpringCloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Deploy-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Deploy-AzSpringCloudApp.md
ms.openlocfilehash: c6a7381c993b52995ab39a60fde54900092a5915
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94262971"
---
# <span data-ttu-id="74eb9-101">Deploy-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="74eb9-101">Deploy-AzSpringCloudApp</span></span>

## <span data-ttu-id="74eb9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="74eb9-102">SYNOPSIS</span></span>
<span data-ttu-id="74eb9-103">Distribuera den inbyggda jar till-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="74eb9-103">Deploy the built jar to service.</span></span>

## <span data-ttu-id="74eb9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="74eb9-104">SYNTAX</span></span>

```
Deploy-AzSpringCloudApp -JarPath <String> -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="74eb9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="74eb9-105">DESCRIPTION</span></span>
<span data-ttu-id="74eb9-106">Distribuera den inbyggda jar till-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="74eb9-106">Deploy the built jar to service.</span></span>

## <span data-ttu-id="74eb9-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="74eb9-107">EXAMPLES</span></span>

### <span data-ttu-id="74eb9-108">Exempel 1: Distribuera lokal kompilerade jar till tjänst med namn.</span><span class="sxs-lookup"><span data-stu-id="74eb9-108">Example 1: Deploy local compiled jar to service by name.</span></span>
```powershell
PS C:\> Deploy-AzSpringCloudApp -ResourceGroupName 'spring-cloud-rg' -ServiceName 'spring-cloud-service' -AppName 'gateway' -JarPath '/home/user/piggymetrics/gateway/target/gateway.jar'

[1/3] Requesting for upload URL
[2/3] Uploading package to blob
[3/3] Updating deployment in app account-service (this operation can take a while to complete)
Name Type
---- ----
prod Microsoft.AppPlatform/Spring/apps/deployments
```

<span data-ttu-id="74eb9-109">Distribuera lokal kompilerade jar till tjänst med namn.</span><span class="sxs-lookup"><span data-stu-id="74eb9-109">Deploy local compiled jar to service by name.</span></span>

## <span data-ttu-id="74eb9-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="74eb9-110">PARAMETERS</span></span>

### <span data-ttu-id="74eb9-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="74eb9-111">-AsJob</span></span>
<span data-ttu-id="74eb9-112">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="74eb9-112">Run the command as a job</span></span>

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

### <span data-ttu-id="74eb9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74eb9-113">-DefaultProfile</span></span>
<span data-ttu-id="74eb9-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="74eb9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74eb9-115">-JarPath</span><span class="sxs-lookup"><span data-stu-id="74eb9-115">-JarPath</span></span>
<span data-ttu-id="74eb9-116">Deploied bevaras.</span><span class="sxs-lookup"><span data-stu-id="74eb9-116">The path of the jar need to be deploied.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74eb9-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="74eb9-117">-Name</span></span>
<span data-ttu-id="74eb9-118">Namnet på program resursen.</span><span class="sxs-lookup"><span data-stu-id="74eb9-118">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AppName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74eb9-119">-Nowait</span><span class="sxs-lookup"><span data-stu-id="74eb9-119">-NoWait</span></span>
<span data-ttu-id="74eb9-120">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="74eb9-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="74eb9-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74eb9-121">-ResourceGroupName</span></span>
<span data-ttu-id="74eb9-122">Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="74eb9-122">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="74eb9-123">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="74eb9-123">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74eb9-124">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="74eb9-124">-ServiceName</span></span>
<span data-ttu-id="74eb9-125">Namnet på tjänst resursen.</span><span class="sxs-lookup"><span data-stu-id="74eb9-125">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74eb9-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="74eb9-126">-SubscriptionId</span></span>
<span data-ttu-id="74eb9-127">Hämtar abonnemangs-ID som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="74eb9-127">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="74eb9-128">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="74eb9-128">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74eb9-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="74eb9-129">-Confirm</span></span>
<span data-ttu-id="74eb9-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="74eb9-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74eb9-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74eb9-131">-WhatIf</span></span>
<span data-ttu-id="74eb9-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="74eb9-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74eb9-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="74eb9-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74eb9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74eb9-134">CommonParameters</span></span>
<span data-ttu-id="74eb9-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74eb9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74eb9-136">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="74eb9-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74eb9-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="74eb9-137">INPUTS</span></span>

## <span data-ttu-id="74eb9-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="74eb9-138">OUTPUTS</span></span>

### <span data-ttu-id="74eb9-139">Microsoft. Azure. PowerShell. cmdletar. SpringCloud. Models. Api20200701. IAppResource</span><span class="sxs-lookup"><span data-stu-id="74eb9-139">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IAppResource</span></span>

## <span data-ttu-id="74eb9-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="74eb9-140">NOTES</span></span>

<span data-ttu-id="74eb9-141">ALIAS</span><span class="sxs-lookup"><span data-stu-id="74eb9-141">ALIASES</span></span>

## <span data-ttu-id="74eb9-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="74eb9-142">RELATED LINKS</span></span>

