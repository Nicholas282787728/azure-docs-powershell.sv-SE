---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azoffice365policyproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzOffice365PolicyProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzOffice365PolicyProperty.md
ms.openlocfilehash: 9fae8c6d543bddc3ad4110b95a1c1b4a1f146879
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323772"
---
# <span data-ttu-id="3356a-101">New-AzOffice365PolicyProperty</span><span class="sxs-lookup"><span data-stu-id="3356a-101">New-AzOffice365PolicyProperty</span></span>

## <span data-ttu-id="3356a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3356a-102">SYNOPSIS</span></span>
<span data-ttu-id="3356a-103">Definiera en ny policy för Office 365-trafik översikten som ska användas med en virtuell enhets webbplats.</span><span class="sxs-lookup"><span data-stu-id="3356a-103">Define a new Office 365 traffic breakout policy to be used with a Virtual Appliance site.</span></span>

## <span data-ttu-id="3356a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3356a-104">SYNTAX</span></span>

```
New-AzOffice365PolicyProperty [-Allow] [-Optimize] [-Default] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3356a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3356a-105">DESCRIPTION</span></span>
<span data-ttu-id="3356a-106">Med kommandot New-AzOffice365PolicyProperties definierar du en princip för Office 365-översikten som ska användas med en virtuell enhets webbplats.</span><span class="sxs-lookup"><span data-stu-id="3356a-106">The New-AzOffice365PolicyProperties command defines an Office 365 breakout policy that is to be used with a Virtual Appliance site.</span></span> 

## <span data-ttu-id="3356a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3356a-107">EXAMPLES</span></span>

### <span data-ttu-id="3356a-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3356a-108">Example 1</span></span>
```powershell
PS C:\> $o365Policy = New-AzOffice365PolicyProperty -Allow -Optimize 
```

<span data-ttu-id="3356a-109">Skapa Office 365-trafiköversikten princip objekt som ska användas med kommandon för den virtuella apparaten webbplats.</span><span class="sxs-lookup"><span data-stu-id="3356a-109">Create Office 365 traffic breakout policy object to be used with Virtual Appliance site commands.</span></span>

## <span data-ttu-id="3356a-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3356a-110">PARAMETERS</span></span>

### <span data-ttu-id="3356a-111">-Tillåt</span><span class="sxs-lookup"><span data-stu-id="3356a-111">-Allow</span></span>
<span data-ttu-id="3356a-112">Översikten Tillåt kategori trafik.</span><span class="sxs-lookup"><span data-stu-id="3356a-112">Breakout the allow category traffic.</span></span>

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

### <span data-ttu-id="3356a-113">-Standard</span><span class="sxs-lookup"><span data-stu-id="3356a-113">-Default</span></span>
<span data-ttu-id="3356a-114">Översikten standard kategori trafik.</span><span class="sxs-lookup"><span data-stu-id="3356a-114">Breakout the default category traffic.</span></span>

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

### <span data-ttu-id="3356a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3356a-115">-DefaultProfile</span></span>
<span data-ttu-id="3356a-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3356a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3356a-117">-Optimera</span><span class="sxs-lookup"><span data-stu-id="3356a-117">-Optimize</span></span>
<span data-ttu-id="3356a-118">Översikten optimera kategori trafik.</span><span class="sxs-lookup"><span data-stu-id="3356a-118">Breakout the optimize category traffic.</span></span>

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

### <span data-ttu-id="3356a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3356a-119">CommonParameters</span></span>
<span data-ttu-id="3356a-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3356a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3356a-121">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3356a-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3356a-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3356a-122">INPUTS</span></span>

### <span data-ttu-id="3356a-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="3356a-123">None</span></span>

## <span data-ttu-id="3356a-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3356a-124">OUTPUTS</span></span>

### <span data-ttu-id="3356a-125">Microsoft. Azure. commands. Networks. Models. PSOffice365PolicyProperties</span><span class="sxs-lookup"><span data-stu-id="3356a-125">Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties</span></span>

## <span data-ttu-id="3356a-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3356a-126">NOTES</span></span>

## <span data-ttu-id="3356a-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3356a-127">RELATED LINKS</span></span>