---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.digitaltwins/get-azdigitaltwinsinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Get-AzDigitalTwinsInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Get-AzDigitalTwinsInstance.md
ms.openlocfilehash: 17e036128dcc6c43044a83d2bbc254cc994ae508
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98402467"
---
# <span data-ttu-id="8d210-101">Get-AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="8d210-101">Get-AzDigitalTwinsInstance</span></span>

## <span data-ttu-id="8d210-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8d210-102">SYNOPSIS</span></span>
<span data-ttu-id="8d210-103">Få DigitalTwinsInstances-resursen.</span><span class="sxs-lookup"><span data-stu-id="8d210-103">Get DigitalTwinsInstances resource.</span></span>

## <span data-ttu-id="8d210-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8d210-104">SYNTAX</span></span>

### <span data-ttu-id="8d210-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="8d210-105">List (Default)</span></span>
```
Get-AzDigitalTwinsInstance [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8d210-106">Lära</span><span class="sxs-lookup"><span data-stu-id="8d210-106">Get</span></span>
```
Get-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8d210-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8d210-107">GetViaIdentity</span></span>
```
Get-AzDigitalTwinsInstance -InputObject <IDigitalTwinsIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="8d210-108">List1</span><span class="sxs-lookup"><span data-stu-id="8d210-108">List1</span></span>
```
Get-AzDigitalTwinsInstance -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="8d210-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8d210-109">DESCRIPTION</span></span>
<span data-ttu-id="8d210-110">Få DigitalTwinsInstances-resursen.</span><span class="sxs-lookup"><span data-stu-id="8d210-110">Get DigitalTwinsInstances resource.</span></span>

## <span data-ttu-id="8d210-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8d210-111">EXAMPLES</span></span>

### <span data-ttu-id="8d210-112">Exempel 1: lista (standard)</span><span class="sxs-lookup"><span data-stu-id="8d210-112">Example 1: List (Default)</span></span>
```powershell
PS C:\> Get-AzDigitalTwinsInstance

Location Name                    Type
-------- ----                    ----
eastus   youriDigitalTwinsTest   Microsoft.DigitalTwins/digitalTwinsInstances
eastus   youriDigitalTwin        Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="8d210-113">Hämta alla DigitalTwinsInstance som standard</span><span class="sxs-lookup"><span data-stu-id="8d210-113">Get all the DigitalTwinsInstance by default</span></span>

### <span data-ttu-id="8d210-114">Exempel 2: get</span><span class="sxs-lookup"><span data-stu-id="8d210-114">Example 2: Get</span></span>
```powershell
PS C:\> Get-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwin

Location Name             Type
-------- ----             ----
eastus   youriDigitalTwin Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="8d210-115">Hämta angivet AzDigitalTwinsInstance av ResourceName</span><span class="sxs-lookup"><span data-stu-id="8d210-115">Get the specified AzDigitalTwinsInstance by ResourceName</span></span>

### <span data-ttu-id="8d210-116">Exempel 3: GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8d210-116">Example 3: GetViaIdentity</span></span>
```powershell
PS C:\> $NewAzDigital = New-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwin -Location eastus
Get-AzDigitalTwinsInstance -inputObject $NewAzDigital

Location Name             Type
-------- ----             ----
eastus   youriDigitalTwin Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="8d210-117">Hämta angivet AzDigitalTwinsInstance efter objekt</span><span class="sxs-lookup"><span data-stu-id="8d210-117">Get the specified AzDigitalTwinsInstance by Object</span></span>

### <span data-ttu-id="8d210-118">Exempel 4: List1</span><span class="sxs-lookup"><span data-stu-id="8d210-118">Example 4: List1</span></span>
```powershell
PS C:\> Get-AzDigitalTwinsInstance -ResourceGroupName youritemp

Location Name                    Type
-------- ----                    ----
eastus   youriDigitalTwinsTest   Microsoft.DigitalTwins/digitalTwinsInstances
eastus   youriDigitalTwin        Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="8d210-119">Skaffa alla DigitalTwinsInstance med ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d210-119">Get all the DigitalTwinsInstance by ResourceGroupName</span></span>

## <span data-ttu-id="8d210-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8d210-120">PARAMETERS</span></span>

### <span data-ttu-id="8d210-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d210-121">-DefaultProfile</span></span>
<span data-ttu-id="8d210-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8d210-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d210-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8d210-123">-InputObject</span></span>
<span data-ttu-id="8d210-124">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="8d210-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8d210-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d210-125">-ResourceGroupName</span></span>
<span data-ttu-id="8d210-126">Namnet på resurs gruppen som innehåller DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="8d210-126">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d210-127">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="8d210-127">-ResourceName</span></span>
<span data-ttu-id="8d210-128">Namnet på DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="8d210-128">The name of the DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d210-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8d210-129">-SubscriptionId</span></span>
<span data-ttu-id="8d210-130">Prenumerations-ID.</span><span class="sxs-lookup"><span data-stu-id="8d210-130">The subscription identifier.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d210-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d210-131">CommonParameters</span></span>
<span data-ttu-id="8d210-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d210-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d210-133">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8d210-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d210-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8d210-134">INPUTS</span></span>

### <span data-ttu-id="8d210-135">Microsoft. Azure. PowerShell. cmdletar. DigitalTwins. Models. IDigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="8d210-135">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span></span>

## <span data-ttu-id="8d210-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8d210-136">OUTPUTS</span></span>

### <span data-ttu-id="8d210-137">Microsoft. Azure. PowerShell. cmdletar. DigitalTwins. Models. Api20201031. IDigitalTwinsDescription</span><span class="sxs-lookup"><span data-stu-id="8d210-137">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span></span>

## <span data-ttu-id="8d210-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8d210-138">NOTES</span></span>

<span data-ttu-id="8d210-139">ALIAS</span><span class="sxs-lookup"><span data-stu-id="8d210-139">ALIASES</span></span>

<span data-ttu-id="8d210-140">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="8d210-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8d210-141">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="8d210-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8d210-142">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8d210-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8d210-143">INPUTOBJECT <IDigitalTwinsIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="8d210-143">INPUTOBJECT <IDigitalTwinsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8d210-144">`[EndpointName <String>]`: Slut punkts resursens namn.</span><span class="sxs-lookup"><span data-stu-id="8d210-144">`[EndpointName <String>]`: Name of Endpoint Resource.</span></span>
  - <span data-ttu-id="8d210-145">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="8d210-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8d210-146">`[Location <String>]`: Plats för DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="8d210-146">`[Location <String>]`: Location of DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="8d210-147">`[ResourceGroupName <String>]`: Namnet på resurs gruppen som innehåller DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="8d210-147">`[ResourceGroupName <String>]`: The name of the resource group that contains the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="8d210-148">`[ResourceName <String>]`: Namnet på DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="8d210-148">`[ResourceName <String>]`: The name of the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="8d210-149">`[SubscriptionId <String>]`: Prenumerationens ID.</span><span class="sxs-lookup"><span data-stu-id="8d210-149">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="8d210-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8d210-150">RELATED LINKS</span></span>

