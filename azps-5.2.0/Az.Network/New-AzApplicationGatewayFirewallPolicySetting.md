---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicysetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicySetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicySetting.md
ms.openlocfilehash: b1665975fd85268bdb8788eb96ba0c8694b6f4c6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98397931"
---
# <span data-ttu-id="d8b6a-101">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="d8b6a-101">New-AzApplicationGatewayFirewallPolicySetting</span></span>

## <span data-ttu-id="d8b6a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d8b6a-102">SYNOPSIS</span></span>
<span data-ttu-id="d8b6a-103">Skapar en princip inställning för brand Väggs principen</span><span class="sxs-lookup"><span data-stu-id="d8b6a-103">Creates a policy setting for the firewall policy</span></span>

## <span data-ttu-id="d8b6a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d8b6a-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicySetting [-Mode <String>] [-State <String>] [-DisableRequestBodyCheck]
 [-MaxRequestBodySizeInKb <Int32>] [-MaxFileUploadInMb <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d8b6a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d8b6a-105">DESCRIPTION</span></span>
<span data-ttu-id="d8b6a-106">Den **nya-AzApplicationGatewayFirewallPolicySetting** skapar ett princip inställningar för en brand Väggs princip.</span><span class="sxs-lookup"><span data-stu-id="d8b6a-106">The **New-AzApplicationGatewayFirewallPolicySetting** creates a policy settings for a firewall policy.</span></span>

## <span data-ttu-id="d8b6a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d8b6a-107">EXAMPLES</span></span>

### <span data-ttu-id="d8b6a-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d8b6a-108">Example 1</span></span>
```powershell
PS C:\> $condition = New-AzApplicationGatewayFirewallPolicySetting -State $enabledState -Mode $enabledMode -DisableRequestBodyCheck -MaxFileUploadInMb $fileUploadLimitInMb -MaxRequestBodySizeInKb $maxRequestBodySizeInKb
```

<span data-ttu-id="d8b6a-109">Kommandot skapar en princip inställning med tillstånd som $enabledState, läge som $enabledMode, RequestBodyCheck som falskt, FileUploadLimitInMb som $fileUploadLimitInMb och MaxRequestBodySizeInKb som $ $maxRequestBodySizeInKb.</span><span class="sxs-lookup"><span data-stu-id="d8b6a-109">The command creates a policy setting with state as $enabledState, mode as $enabledMode, RequestBodyCheck as false, FileUploadLimitInMb as $fileUploadLimitInMb and MaxRequestBodySizeInKb as $$maxRequestBodySizeInKb.</span></span>
<span data-ttu-id="d8b6a-110">Den nya policySettings lagras i $condition.</span><span class="sxs-lookup"><span data-stu-id="d8b6a-110">The new policySettings is stored to $condition.</span></span>

## <span data-ttu-id="d8b6a-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d8b6a-111">PARAMETERS</span></span>

### <span data-ttu-id="d8b6a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8b6a-112">-DefaultProfile</span></span>
<span data-ttu-id="d8b6a-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d8b6a-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8b6a-114">-DisableRequestBodyCheck</span><span class="sxs-lookup"><span data-stu-id="d8b6a-114">-DisableRequestBodyCheck</span></span>
<span data-ttu-id="d8b6a-115">Diables requestBodyCheck i princip inställningar för brand Väggs principen.</span><span class="sxs-lookup"><span data-stu-id="d8b6a-115">Diables the requestBodyCheck in policy settings of the firewall policy.</span></span>

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

### <span data-ttu-id="d8b6a-116">-MaxFileUploadInMb</span><span class="sxs-lookup"><span data-stu-id="d8b6a-116">-MaxFileUploadInMb</span></span>
<span data-ttu-id="d8b6a-117">Maximal fileUpload storlek i MB.</span><span class="sxs-lookup"><span data-stu-id="d8b6a-117">Maximum fileUpload size in MB.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8b6a-118">-MaxRequestBodySizeInKb</span><span class="sxs-lookup"><span data-stu-id="d8b6a-118">-MaxRequestBodySizeInKb</span></span>
<span data-ttu-id="d8b6a-119">MaxRequestBodySizeInKb i princip inställningar för brand Väggs princip.</span><span class="sxs-lookup"><span data-stu-id="d8b6a-119">MaxRequestBodySizeInKb in policy settings of the firewall policy.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 128
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8b6a-120">-Mode</span><span class="sxs-lookup"><span data-stu-id="d8b6a-120">-Mode</span></span>
<span data-ttu-id="d8b6a-121">Brand Väggs läge i princip inställningar för brand Väggs principen.</span><span class="sxs-lookup"><span data-stu-id="d8b6a-121">Firewall Mode in policy settings of the firewall policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Prevention, Detection

Required: False
Position: Named
Default value: Detection
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8b6a-122">-State</span><span class="sxs-lookup"><span data-stu-id="d8b6a-122">-State</span></span>
<span data-ttu-id="d8b6a-123">State-variabel i princip inställningar för brand Väggs principen.</span><span class="sxs-lookup"><span data-stu-id="d8b6a-123">State variable in policy settings of the firewall policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Disabled, Enabled

Required: False
Position: Named
Default value: Enabled
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8b6a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8b6a-124">CommonParameters</span></span>
<span data-ttu-id="d8b6a-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8b6a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8b6a-126">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d8b6a-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8b6a-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d8b6a-127">INPUTS</span></span>

### <span data-ttu-id="d8b6a-128">Ingen</span><span class="sxs-lookup"><span data-stu-id="d8b6a-128">None</span></span>

## <span data-ttu-id="d8b6a-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d8b6a-129">OUTPUTS</span></span>

### <span data-ttu-id="d8b6a-130">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayFirewallPolicySettings</span><span class="sxs-lookup"><span data-stu-id="d8b6a-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicySettings</span></span>

## <span data-ttu-id="d8b6a-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d8b6a-131">NOTES</span></span>

## <span data-ttu-id="d8b6a-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d8b6a-132">RELATED LINKS</span></span>
