---
external help file: ''
Module Name: Azs.Network.Admin
online version: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azsnetworkadminoverview
schema: 2.0.0
ms.openlocfilehash: 8559b8cdde324c3927ac835f49291441a4e58847
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/24/2020
ms.locfileid: "94092940"
---
# <span data-ttu-id="3c3bc-101">Get-AzsNetworkAdminOverview</span><span class="sxs-lookup"><span data-stu-id="3c3bc-101">Get-AzsNetworkAdminOverview</span></span>

## <span data-ttu-id="3c3bc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3c3bc-102">SYNOPSIS</span></span>
<span data-ttu-id="3c3bc-103">Få en översikt över statusen för nätverks resurs leverantören.</span><span class="sxs-lookup"><span data-stu-id="3c3bc-103">Get an overview of the state of the network resource provider.</span></span>

## <span data-ttu-id="3c3bc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3c3bc-104">SYNTAX</span></span>

### <span data-ttu-id="3c3bc-105">Skaffa (standard)</span><span class="sxs-lookup"><span data-stu-id="3c3bc-105">Get (Default)</span></span>
```
Get-AzsNetworkAdminOverview [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3c3bc-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3c3bc-106">GetViaIdentity</span></span>
```
Get-AzsNetworkAdminOverview -InputObject <INetworkAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="3c3bc-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3c3bc-107">DESCRIPTION</span></span>
<span data-ttu-id="3c3bc-108">Få en översikt över statusen för nätverks resurs leverantören.</span><span class="sxs-lookup"><span data-stu-id="3c3bc-108">Get an overview of the state of the network resource provider.</span></span>

## <span data-ttu-id="3c3bc-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3c3bc-109">EXAMPLES</span></span>

### <span data-ttu-id="3c3bc-110">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="3c3bc-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```powershell
Get-AzsNetworkAdminOverview
To view examples, please use the -Online parameter with Get-Help or navigate to: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azsnetworkadminoverview
```



## <span data-ttu-id="3c3bc-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3c3bc-111">PARAMETERS</span></span>

### <span data-ttu-id="3c3bc-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c3bc-112">-DefaultProfile</span></span>
<span data-ttu-id="3c3bc-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3c3bc-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c3bc-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3c3bc-114">-InputObject</span></span>
<span data-ttu-id="3c3bc-115">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="3c3bc-115">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.INetworkAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="3c3bc-116">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3c3bc-116">-SubscriptionId</span></span>
<span data-ttu-id="3c3bc-117">Autentiseringsuppgifter för prenumerationer som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="3c3bc-117">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="3c3bc-118">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="3c3bc-118">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3c3bc-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c3bc-119">CommonParameters</span></span>
<span data-ttu-id="3c3bc-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c3bc-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c3bc-121">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3c3bc-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c3bc-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3c3bc-122">INPUTS</span></span>

### <span data-ttu-id="3c3bc-123">Microsoft. Azure. PowerShell. cmdletar. NetworkAdmin. Models. INetworkAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="3c3bc-123">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.INetworkAdminIdentity</span></span>

## <span data-ttu-id="3c3bc-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3c3bc-124">OUTPUTS</span></span>

### <span data-ttu-id="3c3bc-125">Microsoft. Azure. PowerShell. cmdletar. NetworkAdmin. Models. Api20150615. IAdminOverview</span><span class="sxs-lookup"><span data-stu-id="3c3bc-125">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IAdminOverview</span></span>



## <span data-ttu-id="3c3bc-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3c3bc-126">NOTES</span></span>

<span data-ttu-id="3c3bc-127">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="3c3bc-127">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3c3bc-128">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3c3bc-128">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="3c3bc-129">INPUTOBJECT <INetworkAdminIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="3c3bc-129">INPUTOBJECT <INetworkAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3c3bc-130">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="3c3bc-130">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3c3bc-131">`[Location <String>]`: Resursens plats.</span><span class="sxs-lookup"><span data-stu-id="3c3bc-131">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="3c3bc-132">`[ResourceName <String>]`: Namnet på resursen.</span><span class="sxs-lookup"><span data-stu-id="3c3bc-132">`[ResourceName <String>]`: Name of the resource.</span></span>
  - <span data-ttu-id="3c3bc-133">`[SubscriptionId <String>]`: Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="3c3bc-133">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="3c3bc-134">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="3c3bc-134">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="3c3bc-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3c3bc-135">RELATED LINKS</span></span>
