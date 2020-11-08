---
external help file: ''
Module Name: Azs.Network.Admin
online version: https://docs.microsoft.com/powershell/module/azs.network.admin/remove-azsnetworkquota
schema: 2.0.0
ms.openlocfilehash: fe7c391b8f15e3389a9d61070b8f55d47af6d6ec
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/24/2020
ms.locfileid: "94092968"
---
# <span data-ttu-id="30f96-101">Remove-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="30f96-101">Remove-AzsNetworkQuota</span></span>

## <span data-ttu-id="30f96-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="30f96-102">SYNOPSIS</span></span>
<span data-ttu-id="30f96-103">Ta bort en kvot med namn.</span><span class="sxs-lookup"><span data-stu-id="30f96-103">Delete a quota by name.</span></span>

## <span data-ttu-id="30f96-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="30f96-104">SYNTAX</span></span>

### <span data-ttu-id="30f96-105">Ta bort (standard)</span><span class="sxs-lookup"><span data-stu-id="30f96-105">Delete (Default)</span></span>
```
Remove-AzsNetworkQuota -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="30f96-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="30f96-106">DeleteViaIdentity</span></span>
```
Remove-AzsNetworkQuota -InputObject <INetworkAdminIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="30f96-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="30f96-107">DESCRIPTION</span></span>
<span data-ttu-id="30f96-108">Ta bort en kvot med namn.</span><span class="sxs-lookup"><span data-stu-id="30f96-108">Delete a quota by name.</span></span>

## <span data-ttu-id="30f96-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="30f96-109">EXAMPLES</span></span>

### <span data-ttu-id="30f96-110">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="30f96-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="30f96-111">Ta bort en nätverks kvot efter namn.</span><span class="sxs-lookup"><span data-stu-id="30f96-111">Remove a network quota by name.</span></span>

### <span data-ttu-id="30f96-112">--------------------------EXEMPEL 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="30f96-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsNetworkQuota -Name NetworkQuota1 | Remove-AzsNetworkQuota
```

<span data-ttu-id="30f96-113">Ta bort en nätverks kvot med en pipe.</span><span class="sxs-lookup"><span data-stu-id="30f96-113">Remove a network quota using a pipe.</span></span>

### <span data-ttu-id="30f96-114">--------------------------EXEMPEL 3--------------------------</span><span class="sxs-lookup"><span data-stu-id="30f96-114">-------------------------- EXAMPLE 3 --------------------------</span></span>
```
Remove-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="30f96-115">Ta bort en nätverks kvot.</span><span class="sxs-lookup"><span data-stu-id="30f96-115">Remove a network quota.</span></span>

## <span data-ttu-id="30f96-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="30f96-116">PARAMETERS</span></span>

### <span data-ttu-id="30f96-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="30f96-117">-AsJob</span></span>
<span data-ttu-id="30f96-118">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="30f96-118">Run the command as a job</span></span>

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

### <span data-ttu-id="30f96-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30f96-119">-DefaultProfile</span></span>
<span data-ttu-id="30f96-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="30f96-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30f96-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="30f96-121">-InputObject</span></span>
<span data-ttu-id="30f96-122">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="30f96-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.INetworkAdminIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="30f96-123">-Plats</span><span class="sxs-lookup"><span data-stu-id="30f96-123">-Location</span></span>
<span data-ttu-id="30f96-124">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="30f96-124">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Name
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="30f96-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="30f96-125">-Name</span></span>
<span data-ttu-id="30f96-126">Namnet på resursen.</span><span class="sxs-lookup"><span data-stu-id="30f96-126">Name of the resource.</span></span>

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

### <span data-ttu-id="30f96-127">-Nowait</span><span class="sxs-lookup"><span data-stu-id="30f96-127">-NoWait</span></span>
<span data-ttu-id="30f96-128">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="30f96-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="30f96-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="30f96-129">-PassThru</span></span>
<span data-ttu-id="30f96-130">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="30f96-130">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="30f96-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="30f96-131">-SubscriptionId</span></span>
<span data-ttu-id="30f96-132">Autentiseringsuppgifter för prenumerationer som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="30f96-132">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="30f96-133">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="30f96-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="30f96-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="30f96-134">-Confirm</span></span>
<span data-ttu-id="30f96-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="30f96-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30f96-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30f96-136">-WhatIf</span></span>
<span data-ttu-id="30f96-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="30f96-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30f96-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="30f96-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30f96-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30f96-139">CommonParameters</span></span>
<span data-ttu-id="30f96-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30f96-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30f96-141">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="30f96-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30f96-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="30f96-142">INPUTS</span></span>

### <span data-ttu-id="30f96-143">Microsoft. Azure. PowerShell. cmdletar. NetworkAdmin. Models. INetworkAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="30f96-143">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.INetworkAdminIdentity</span></span>

## <span data-ttu-id="30f96-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="30f96-144">OUTPUTS</span></span>

### <span data-ttu-id="30f96-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="30f96-145">System.Boolean</span></span>



## <span data-ttu-id="30f96-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="30f96-146">NOTES</span></span>

<span data-ttu-id="30f96-147">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="30f96-147">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="30f96-148">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="30f96-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="30f96-149">INPUTOBJECT <INetworkAdminIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="30f96-149">INPUTOBJECT <INetworkAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="30f96-150">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="30f96-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="30f96-151">`[Location <String>]`: Resursens plats.</span><span class="sxs-lookup"><span data-stu-id="30f96-151">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="30f96-152">`[ResourceName <String>]`: Namnet på resursen.</span><span class="sxs-lookup"><span data-stu-id="30f96-152">`[ResourceName <String>]`: Name of the resource.</span></span>
  - <span data-ttu-id="30f96-153">`[SubscriptionId <String>]`: Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="30f96-153">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="30f96-154">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="30f96-154">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="30f96-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="30f96-155">RELATED LINKS</span></span>
