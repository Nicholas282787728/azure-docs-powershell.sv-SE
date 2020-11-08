---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azoffice365policyproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzOffice365PolicyProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzOffice365PolicyProperty.md
ms.openlocfilehash: 82ff7d915a7ddc2d15655513dade28fc1e7ffff0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94262542"
---
# <span data-ttu-id="bfdbd-101">New-AzOffice365PolicyProperty</span><span class="sxs-lookup"><span data-stu-id="bfdbd-101">New-AzOffice365PolicyProperty</span></span>

## <span data-ttu-id="bfdbd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bfdbd-102">SYNOPSIS</span></span>
<span data-ttu-id="bfdbd-103">Definiera en ny policy för Office 365-trafik översikten som ska användas med en virtuell enhets webbplats.</span><span class="sxs-lookup"><span data-stu-id="bfdbd-103">Define a new Office 365 traffic breakout policy to be used with a Virtual Appliance site.</span></span>

## <span data-ttu-id="bfdbd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bfdbd-104">SYNTAX</span></span>

```
New-AzOffice365PolicyProperty [-Allow] [-Optimize] [-Default] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bfdbd-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bfdbd-105">DESCRIPTION</span></span>
<span data-ttu-id="bfdbd-106">Med kommandot New-AzOffice365PolicyProperties definierar du en princip för Office 365-översikten som ska användas woith en virtuell enhets webbplats.</span><span class="sxs-lookup"><span data-stu-id="bfdbd-106">The New-AzOffice365PolicyProperties command defines an Office 365 breakout policy that is to be used woith a Virtual Appliance site.</span></span> 

## <span data-ttu-id="bfdbd-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bfdbd-107">EXAMPLES</span></span>

### <span data-ttu-id="bfdbd-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="bfdbd-108">Example 1</span></span>
```powershell
PS C:\> $o365Policy = New-AzOffice365PolicyProperty -Allow -Optimize 
```

<span data-ttu-id="bfdbd-109">Skapa Office 365-trafiköversikten princip objekt som ska användas med kommandon för den virtuella apparaten webbplats.</span><span class="sxs-lookup"><span data-stu-id="bfdbd-109">Create Office 365 traffic breakout policy object to be used with Virtual Appliance site commands.</span></span>

## <span data-ttu-id="bfdbd-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bfdbd-110">PARAMETERS</span></span>

### <span data-ttu-id="bfdbd-111">-Tillåt</span><span class="sxs-lookup"><span data-stu-id="bfdbd-111">-Allow</span></span>
<span data-ttu-id="bfdbd-112">Översikten Tillåt kategori trafik.</span><span class="sxs-lookup"><span data-stu-id="bfdbd-112">Breakout the allow category traffic.</span></span>

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

### <span data-ttu-id="bfdbd-113">-Standard</span><span class="sxs-lookup"><span data-stu-id="bfdbd-113">-Default</span></span>
<span data-ttu-id="bfdbd-114">Översikten standard kategori trafik.</span><span class="sxs-lookup"><span data-stu-id="bfdbd-114">Breakout the default category traffic.</span></span>

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

### <span data-ttu-id="bfdbd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfdbd-115">-DefaultProfile</span></span>
<span data-ttu-id="bfdbd-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bfdbd-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bfdbd-117">-Optimera</span><span class="sxs-lookup"><span data-stu-id="bfdbd-117">-Optimize</span></span>
<span data-ttu-id="bfdbd-118">Översikten optimera kategori trafik.</span><span class="sxs-lookup"><span data-stu-id="bfdbd-118">Breakout the optimize category traffic.</span></span>

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

### <span data-ttu-id="bfdbd-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfdbd-119">CommonParameters</span></span>
<span data-ttu-id="bfdbd-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bfdbd-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfdbd-121">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bfdbd-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfdbd-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bfdbd-122">INPUTS</span></span>

### <span data-ttu-id="bfdbd-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="bfdbd-123">None</span></span>

## <span data-ttu-id="bfdbd-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bfdbd-124">OUTPUTS</span></span>

### <span data-ttu-id="bfdbd-125">Microsoft. Azure. commands. Networks. Models. PSOffice365PolicyProperties</span><span class="sxs-lookup"><span data-stu-id="bfdbd-125">Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties</span></span>

## <span data-ttu-id="bfdbd-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bfdbd-126">NOTES</span></span>

## <span data-ttu-id="bfdbd-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bfdbd-127">RELATED LINKS</span></span>
