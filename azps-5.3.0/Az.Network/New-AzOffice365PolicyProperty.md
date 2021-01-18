---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azoffice365policyproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzOffice365PolicyProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzOffice365PolicyProperty.md
ms.openlocfilehash: 9fae8c6d543bddc3ad4110b95a1c1b4a1f146879
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98521855"
---
# <span data-ttu-id="f413e-101">New-AzOffice365PolicyProperty</span><span class="sxs-lookup"><span data-stu-id="f413e-101">New-AzOffice365PolicyProperty</span></span>

## <span data-ttu-id="f413e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f413e-102">SYNOPSIS</span></span>
<span data-ttu-id="f413e-103">Definiera en ny policy för Office 365-trafik översikten som ska användas med en virtuell enhets webbplats.</span><span class="sxs-lookup"><span data-stu-id="f413e-103">Define a new Office 365 traffic breakout policy to be used with a Virtual Appliance site.</span></span>

## <span data-ttu-id="f413e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f413e-104">SYNTAX</span></span>

```
New-AzOffice365PolicyProperty [-Allow] [-Optimize] [-Default] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f413e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f413e-105">DESCRIPTION</span></span>
<span data-ttu-id="f413e-106">Med kommandot New-AzOffice365PolicyProperties definierar du en princip för Office 365-översikten som ska användas med en virtuell enhets webbplats.</span><span class="sxs-lookup"><span data-stu-id="f413e-106">The New-AzOffice365PolicyProperties command defines an Office 365 breakout policy that is to be used with a Virtual Appliance site.</span></span> 

## <span data-ttu-id="f413e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f413e-107">EXAMPLES</span></span>

### <span data-ttu-id="f413e-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f413e-108">Example 1</span></span>
```powershell
PS C:\> $o365Policy = New-AzOffice365PolicyProperty -Allow -Optimize 
```

<span data-ttu-id="f413e-109">Skapa Office 365-trafiköversikten princip objekt som ska användas med kommandon för den virtuella apparaten webbplats.</span><span class="sxs-lookup"><span data-stu-id="f413e-109">Create Office 365 traffic breakout policy object to be used with Virtual Appliance site commands.</span></span>

## <span data-ttu-id="f413e-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f413e-110">PARAMETERS</span></span>

### <span data-ttu-id="f413e-111">-Tillåt</span><span class="sxs-lookup"><span data-stu-id="f413e-111">-Allow</span></span>
<span data-ttu-id="f413e-112">Översikten Tillåt kategori trafik.</span><span class="sxs-lookup"><span data-stu-id="f413e-112">Breakout the allow category traffic.</span></span>

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

### <span data-ttu-id="f413e-113">-Standard</span><span class="sxs-lookup"><span data-stu-id="f413e-113">-Default</span></span>
<span data-ttu-id="f413e-114">Översikten standard kategori trafik.</span><span class="sxs-lookup"><span data-stu-id="f413e-114">Breakout the default category traffic.</span></span>

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

### <span data-ttu-id="f413e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f413e-115">-DefaultProfile</span></span>
<span data-ttu-id="f413e-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f413e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f413e-117">-Optimera</span><span class="sxs-lookup"><span data-stu-id="f413e-117">-Optimize</span></span>
<span data-ttu-id="f413e-118">Översikten optimera kategori trafik.</span><span class="sxs-lookup"><span data-stu-id="f413e-118">Breakout the optimize category traffic.</span></span>

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

### <span data-ttu-id="f413e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f413e-119">CommonParameters</span></span>
<span data-ttu-id="f413e-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f413e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f413e-121">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f413e-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f413e-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f413e-122">INPUTS</span></span>

### <span data-ttu-id="f413e-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="f413e-123">None</span></span>

## <span data-ttu-id="f413e-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f413e-124">OUTPUTS</span></span>

### <span data-ttu-id="f413e-125">Microsoft. Azure. commands. Networks. Models. PSOffice365PolicyProperties</span><span class="sxs-lookup"><span data-stu-id="f413e-125">Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties</span></span>

## <span data-ttu-id="f413e-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f413e-126">NOTES</span></span>

## <span data-ttu-id="f413e-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f413e-127">RELATED LINKS</span></span>
