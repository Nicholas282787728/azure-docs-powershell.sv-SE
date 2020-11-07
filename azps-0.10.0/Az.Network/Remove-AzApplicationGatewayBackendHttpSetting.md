---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-AzApplicationGatewayBackendHttpSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayBackendHttpSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayBackendHttpSetting.md
ms.openlocfilehash: 168223e9e442b7aa37da11f3a1e0a092c3cb3efc
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922067"
---
# <span data-ttu-id="35b5c-101">Remove-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="35b5c-101">Remove-AzApplicationGatewayBackendHttpSetting</span></span>

## <span data-ttu-id="35b5c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="35b5c-102">SYNOPSIS</span></span>
<span data-ttu-id="35b5c-103">Tar bort backend-HTTP-inställningar från en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="35b5c-103">Removes back-end HTTP settings from an application gateway.</span></span>

## <span data-ttu-id="35b5c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="35b5c-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayBackendHttpSetting -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="35b5c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="35b5c-105">DESCRIPTION</span></span>
<span data-ttu-id="35b5c-106">Remove-AzApplicationGatewayBackendHttpSetting cmdlet tar bort backend-inställningarna från en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="35b5c-106">The Remove-AzApplicationGatewayBackendHttpSetting cmdlet removes back-end Hypertext Transfer Protocol (HTTP) settings from an Azure application gateway.</span></span>

## <span data-ttu-id="35b5c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="35b5c-107">EXAMPLES</span></span>

### <span data-ttu-id="35b5c-108">Exempel 1: ta bort backend-HTTP-inställningar från en Programgateway</span><span class="sxs-lookup"><span data-stu-id="35b5c-108">Example 1: Remove back-end HTTP settings from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayBackendHttpSetting -ApplicationGateway $AppGw -Name "BackEndSetting02"
```

<span data-ttu-id="35b5c-109">Det första kommandot får en Programgateway som heter ApplicationGateway01 som tillhör resurs gruppen med namnet ResourceGroup01 och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="35b5c-109">The first command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="35b5c-110">Med det andra kommandot tas backend-HTTP-inställningen bort med namnet BackEndSetting02 från Application Gateway som lagras i $AppGw.</span><span class="sxs-lookup"><span data-stu-id="35b5c-110">The second command removes the back-end HTTP setting named BackEndSetting02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="35b5c-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="35b5c-111">PARAMETERS</span></span>

### <span data-ttu-id="35b5c-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="35b5c-112">-ApplicationGateway</span></span>
<span data-ttu-id="35b5c-113">Anger den Programgateway från vilken denna cmdlet tar bort backend HTTP-inställningar.</span><span class="sxs-lookup"><span data-stu-id="35b5c-113">Specifies the application gateway from which this cmdlet removes back-end HTTP settings.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="35b5c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35b5c-114">-DefaultProfile</span></span>
<span data-ttu-id="35b5c-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="35b5c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35b5c-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="35b5c-116">-Name</span></span>
<span data-ttu-id="35b5c-117">Anger namnet på de HTTP-inställningar för backend som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="35b5c-117">Specifies the name of the back-end HTTP settings that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35b5c-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35b5c-118">CommonParameters</span></span>
<span data-ttu-id="35b5c-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35b5c-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35b5c-120">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35b5c-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35b5c-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="35b5c-121">INPUTS</span></span>

### <span data-ttu-id="35b5c-122">System. String</span><span class="sxs-lookup"><span data-stu-id="35b5c-122">System.String</span></span>

## <span data-ttu-id="35b5c-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="35b5c-123">OUTPUTS</span></span>

### <span data-ttu-id="35b5c-124">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="35b5c-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="35b5c-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="35b5c-125">NOTES</span></span>

## <span data-ttu-id="35b5c-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="35b5c-126">RELATED LINKS</span></span>

[<span data-ttu-id="35b5c-127">Add-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="35b5c-127">Add-AzApplicationGatewayBackendHttpSetting</span></span>]()

[<span data-ttu-id="35b5c-128">New-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="35b5c-128">New-AzApplicationGatewayBackendHttpSetting</span></span>]()

[<span data-ttu-id="35b5c-129">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="35b5c-129">Get-AzApplicationGatewayBackendHttpSetting</span></span>]()

[<span data-ttu-id="35b5c-130">Set-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="35b5c-130">Set-AzApplicationGatewayBackendHttpSetting</span></span>]()

