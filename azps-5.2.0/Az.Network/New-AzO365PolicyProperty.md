---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azo365policyproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzO365PolicyProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzO365PolicyProperty.md
ms.openlocfilehash: 2aeb26447c5684b57d966c403a256fe3d1361a41
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98390768"
---
# <span data-ttu-id="7f8f7-101">New-AzO365PolicyProperty</span><span class="sxs-lookup"><span data-stu-id="7f8f7-101">New-AzO365PolicyProperty</span></span>

## <span data-ttu-id="7f8f7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7f8f7-102">SYNOPSIS</span></span>
<span data-ttu-id="7f8f7-103">Skapa ett princip objekt för Office 365-översikten.</span><span class="sxs-lookup"><span data-stu-id="7f8f7-103">Create an office 365 traffic breakout policy object.</span></span>

## <span data-ttu-id="7f8f7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7f8f7-104">SYNTAX</span></span>

```
New-AzO365PolicyProperty [-Allow] [-Optimize] [-Default] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7f8f7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7f8f7-105">DESCRIPTION</span></span>
<span data-ttu-id="7f8f7-106">Skapa en princip för Office 365-översikten som ska användas med New-AzVpnSite och Update-AzVpnSite cmdletar.</span><span class="sxs-lookup"><span data-stu-id="7f8f7-106">Create an office 365 breakout policy to be used with New-AzVpnSite and Update-AzVpnSite cmdlets.</span></span>
## <span data-ttu-id="7f8f7-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7f8f7-107">EXAMPLES</span></span>

### <span data-ttu-id="7f8f7-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7f8f7-108">Example 1</span></span>
```powershell
PS C:\> $policy = New-AzO365PolicyProperty -Allow -Optimize
```

<span data-ttu-id="7f8f7-109">Skapa en policy för Office 365-översikten med översikten som tillåts för att tillåta och optimera trafik kategorin.</span><span class="sxs-lookup"><span data-stu-id="7f8f7-109">Create an office 365 traffic breakout policy with breakout allowed for allow and optimize category of traffic.</span></span>

## <span data-ttu-id="7f8f7-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7f8f7-110">PARAMETERS</span></span>

### <span data-ttu-id="7f8f7-111">-Tillåt</span><span class="sxs-lookup"><span data-stu-id="7f8f7-111">-Allow</span></span>
<span data-ttu-id="7f8f7-112">Översikten Tillåt kategori trafik.</span><span class="sxs-lookup"><span data-stu-id="7f8f7-112">Breakout the allow category traffic.</span></span>

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

### <span data-ttu-id="7f8f7-113">-Standard</span><span class="sxs-lookup"><span data-stu-id="7f8f7-113">-Default</span></span>
<span data-ttu-id="7f8f7-114">Översikten standard kategori trafik.</span><span class="sxs-lookup"><span data-stu-id="7f8f7-114">Breakout the default category traffic.</span></span>

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

### <span data-ttu-id="7f8f7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f8f7-115">-DefaultProfile</span></span>
<span data-ttu-id="7f8f7-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7f8f7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f8f7-117">-Optimera</span><span class="sxs-lookup"><span data-stu-id="7f8f7-117">-Optimize</span></span>
<span data-ttu-id="7f8f7-118">Översikten optimera kategori trafik.</span><span class="sxs-lookup"><span data-stu-id="7f8f7-118">Breakout the optimize category traffic.</span></span>

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

### <span data-ttu-id="7f8f7-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f8f7-119">CommonParameters</span></span>
<span data-ttu-id="7f8f7-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f8f7-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f8f7-121">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7f8f7-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f8f7-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7f8f7-122">INPUTS</span></span>

### <span data-ttu-id="7f8f7-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="7f8f7-123">None</span></span>

## <span data-ttu-id="7f8f7-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7f8f7-124">OUTPUTS</span></span>

### <span data-ttu-id="7f8f7-125">Microsoft. Azure. commands. Networks. Models. PSO365PolicyProperties</span><span class="sxs-lookup"><span data-stu-id="7f8f7-125">Microsoft.Azure.Commands.Network.Models.PSO365PolicyProperties</span></span>

## <span data-ttu-id="7f8f7-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7f8f7-126">NOTES</span></span>

## <span data-ttu-id="7f8f7-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7f8f7-127">RELATED LINKS</span></span>
