---
external help file: ''
Module Name: Az.ConnectedKubernetes
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedkubernetes/remove-azconnectedkubernetes
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Remove-AzConnectedKubernetes.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Remove-AzConnectedKubernetes.md
ms.openlocfilehash: 4bc5c82bbfb930484a4a3541e7e97b68ce9be2e1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258887"
---
# <span data-ttu-id="d583c-101">Remove-AzConnectedKubernetes</span><span class="sxs-lookup"><span data-stu-id="d583c-101">Remove-AzConnectedKubernetes</span></span>

## <span data-ttu-id="d583c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d583c-102">SYNOPSIS</span></span>
<span data-ttu-id="d583c-103">Ta bort ett anslutet kluster och ta bort den spårade resursen i en Azure Resource Manager (ARM).</span><span class="sxs-lookup"><span data-stu-id="d583c-103">Delete a connected cluster, removing the tracked resource in Azure Resource Manager (ARM).</span></span>

## <span data-ttu-id="d583c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d583c-104">SYNTAX</span></span>

### <span data-ttu-id="d583c-105">Ta bort (standard)</span><span class="sxs-lookup"><span data-stu-id="d583c-105">Delete (Default)</span></span>
```
Remove-AzConnectedKubernetes -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-KubeConfig <String>] [-KubeContext <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d583c-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d583c-106">DeleteViaIdentity</span></span>
```
Remove-AzConnectedKubernetes -InputObject <IConnectedKubernetesIdentity> [-KubeConfig <String>]
 [-KubeContext <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="d583c-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d583c-107">DESCRIPTION</span></span>
<span data-ttu-id="d583c-108">Ta bort ett anslutet kluster och ta bort den spårade resursen i en Azure Resource Manager (ARM).</span><span class="sxs-lookup"><span data-stu-id="d583c-108">Delete a connected cluster, removing the tracked resource in Azure Resource Manager (ARM).</span></span>

## <span data-ttu-id="d583c-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d583c-109">EXAMPLES</span></span>

### <span data-ttu-id="d583c-110">Exempel 1: ta bort en ansluten Kubernetes</span><span class="sxs-lookup"><span data-stu-id="d583c-110">Example 1: Remove a connected kubernetes</span></span>
```powershell
PS C:\> Remove-AzConnectedKubernetes -ResourceGroupName azureps-manual-test -ClusterName ps-connaks-t01

```

<span data-ttu-id="d583c-111">Det här kommandot tar bort en ansluten Kubernetes</span><span class="sxs-lookup"><span data-stu-id="d583c-111">This command removes a connected kubernetes</span></span>

### <span data-ttu-id="d583c-112">Exempel 2: ta bort en ansluten Kubernetes efter objekt</span><span class="sxs-lookup"><span data-stu-id="d583c-112">Example 2: Remove a connected kubernetes by object</span></span>
```powershell
PS C:\> $connaks = Get-AzConnectedKubernetes -ResourceGroupName azureps-manual-test -Name ps-connaks-t02
PS C:\> Remove-AzConnectedKubernetes -InputObject $connaks

```

<span data-ttu-id="d583c-113">Det här kommandot tar bort en ansluten Kubernetes efter objekt</span><span class="sxs-lookup"><span data-stu-id="d583c-113">This command removes a connected kubernetes by object</span></span>

## <span data-ttu-id="d583c-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d583c-114">PARAMETERS</span></span>

### <span data-ttu-id="d583c-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d583c-115">-AsJob</span></span>
<span data-ttu-id="d583c-116">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="d583c-116">Run the command as a job</span></span>

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

### <span data-ttu-id="d583c-117">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="d583c-117">-ClusterName</span></span>
<span data-ttu-id="d583c-118">Namnet på det Kubernetes-kluster där get anropas.</span><span class="sxs-lookup"><span data-stu-id="d583c-118">The name of the Kubernetes cluster on which get is called.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d583c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d583c-119">-DefaultProfile</span></span>
<span data-ttu-id="d583c-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d583c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d583c-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d583c-121">-InputObject</span></span>
<span data-ttu-id="d583c-122">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="d583c-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d583c-123">-KubeConfig</span><span class="sxs-lookup"><span data-stu-id="d583c-123">-KubeConfig</span></span>
<span data-ttu-id="d583c-124">Sökvägen till Kube-konfigurations filen</span><span class="sxs-lookup"><span data-stu-id="d583c-124">Path to the kube config file</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d583c-125">-KubeContext</span><span class="sxs-lookup"><span data-stu-id="d583c-125">-KubeContext</span></span>
<span data-ttu-id="d583c-126">Kubconfig kontext från aktuell dator</span><span class="sxs-lookup"><span data-stu-id="d583c-126">Kubconfig context from current machine</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d583c-127">-Nowait</span><span class="sxs-lookup"><span data-stu-id="d583c-127">-NoWait</span></span>
<span data-ttu-id="d583c-128">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="d583c-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d583c-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d583c-129">-PassThru</span></span>
<span data-ttu-id="d583c-130">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="d583c-130">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="d583c-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d583c-131">-ResourceGroupName</span></span>
<span data-ttu-id="d583c-132">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="d583c-132">The name of the resource group.</span></span>
<span data-ttu-id="d583c-133">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="d583c-133">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d583c-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d583c-134">-SubscriptionId</span></span>
<span data-ttu-id="d583c-135">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="d583c-135">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d583c-136">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d583c-136">-Confirm</span></span>
<span data-ttu-id="d583c-137">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d583c-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d583c-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d583c-138">-WhatIf</span></span>
<span data-ttu-id="d583c-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d583c-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d583c-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d583c-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d583c-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d583c-141">CommonParameters</span></span>
<span data-ttu-id="d583c-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d583c-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d583c-143">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d583c-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d583c-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d583c-144">INPUTS</span></span>

### <span data-ttu-id="d583c-145">Microsoft. Azure. PowerShell. cmdletar. ConnectedKubernetes. Models. IConnectedKubernetesIdentity</span><span class="sxs-lookup"><span data-stu-id="d583c-145">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity</span></span>

## <span data-ttu-id="d583c-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d583c-146">OUTPUTS</span></span>

### <span data-ttu-id="d583c-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d583c-147">System.Boolean</span></span>

## <span data-ttu-id="d583c-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d583c-148">NOTES</span></span>

<span data-ttu-id="d583c-149">ALIAS</span><span class="sxs-lookup"><span data-stu-id="d583c-149">ALIASES</span></span>

<span data-ttu-id="d583c-150">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="d583c-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d583c-151">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="d583c-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d583c-152">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d583c-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d583c-153">INPUTOBJECT <IConnectedKubernetesIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="d583c-153">INPUTOBJECT <IConnectedKubernetesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d583c-154">`[ClusterName <String>]`: Namnet på det Kubernetes-kluster där get anropas.</span><span class="sxs-lookup"><span data-stu-id="d583c-154">`[ClusterName <String>]`: The name of the Kubernetes cluster on which get is called.</span></span>
  - <span data-ttu-id="d583c-155">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="d583c-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d583c-156">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="d583c-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="d583c-157">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="d583c-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="d583c-158">`[SubscriptionId <String>]`: Mål prenumerationens ID.</span><span class="sxs-lookup"><span data-stu-id="d583c-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="d583c-159">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d583c-159">RELATED LINKS</span></span>

