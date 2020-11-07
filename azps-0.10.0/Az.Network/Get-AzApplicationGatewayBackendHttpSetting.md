---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-AzApplicationGatewayBackendHttpSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayBackendHttpSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayBackendHttpSetting.md
ms.openlocfilehash: 96872aa399c3241710e12e3b96a14e8678f21d83
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922336"
---
# <span data-ttu-id="b57dc-101">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="b57dc-101">Get-AzApplicationGatewayBackendHttpSetting</span></span>

## <span data-ttu-id="b57dc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b57dc-102">SYNOPSIS</span></span>
<span data-ttu-id="b57dc-103">Hämtar dina backend HTTP-inställningar för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="b57dc-103">Gets the back-end HTTP settings of an application gateway.</span></span>

## <span data-ttu-id="b57dc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b57dc-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayBackendHttpSetting [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b57dc-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b57dc-105">DESCRIPTION</span></span>
<span data-ttu-id="b57dc-106">Med cmdleten Get-AzApplicationGatewayBackendHttpSetting får du backend-HTTP-inställningarna för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="b57dc-106">The Get-AzApplicationGatewayBackendHttpSetting cmdlet gets the back-end HTTP settings of an application gateway.</span></span>

## <span data-ttu-id="b57dc-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b57dc-107">EXAMPLES</span></span>

### <span data-ttu-id="b57dc-108">Exempel 1: kom tillbaka-HTTP-inställningar efter namn</span><span class="sxs-lookup"><span data-stu-id="b57dc-108">Example 1: Get back-end HTTP settings by name</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzApplicationGatewayBackendHttpSetting -Name "Settings01" -ApplicationGateway $AppGw
```

<span data-ttu-id="b57dc-109">Det första kommandot får den Programgateway som heter ApplicationGateway01 i resurs gruppen som heter ResourceGroup01 och lagrar den i $AppGw variabel. Det andra kommandot får HTTP-inställningarna "Settings01" för $AppGw och lagrar inställningarna i $Settings-variabeln.</span><span class="sxs-lookup"><span data-stu-id="b57dc-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>

### <span data-ttu-id="b57dc-110">Exempel 2: få en samling backend-HTTP-inställningar</span><span class="sxs-lookup"><span data-stu-id="b57dc-110">Example 2: Get a collection of back-end HTTP settings</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SettingsList  = Get-AzApplicationGatewayBackendHttpSetting -ApplicationGateway $AppGw
```

<span data-ttu-id="b57dc-111">Det första kommandot får den Programgateway som heter ApplicationGateway01 i resurs gruppen som heter ResourceGroup01 och lagrar den i $AppGw variabel. Det andra kommandot hämtar HTTP-inställningarna för $AppGw och lagrar inställningarna i $SettingsList-variabeln.</span><span class="sxs-lookup"><span data-stu-id="b57dc-111">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the collection of HTTP settings for $AppGw and stores the settings in the $SettingsList variable.</span></span>

## <span data-ttu-id="b57dc-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b57dc-112">PARAMETERS</span></span>

### <span data-ttu-id="b57dc-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b57dc-113">-ApplicationGateway</span></span>
<span data-ttu-id="b57dc-114">Anger ett objekt för Application Gateway som innehåller backend HTTP-inställningar.</span><span class="sxs-lookup"><span data-stu-id="b57dc-114">Specifies an application gateway object that contains back-end HTTP settings.</span></span>

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

### <span data-ttu-id="b57dc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b57dc-115">-DefaultProfile</span></span>
<span data-ttu-id="b57dc-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b57dc-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b57dc-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="b57dc-117">-Name</span></span>
<span data-ttu-id="b57dc-118">Anger namnet på Server delens HTTP-inställningar som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="b57dc-118">Specifies the name of the backend HTTP settings that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b57dc-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b57dc-119">CommonParameters</span></span>
<span data-ttu-id="b57dc-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b57dc-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b57dc-121">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b57dc-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b57dc-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b57dc-122">INPUTS</span></span>

### <span data-ttu-id="b57dc-123">System. String</span><span class="sxs-lookup"><span data-stu-id="b57dc-123">System.String</span></span>

## <span data-ttu-id="b57dc-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b57dc-124">OUTPUTS</span></span>

### <span data-ttu-id="b57dc-125">Microsoft. Azure. commands. Networks. Models. AzureApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="b57dc-125">Microsoft.Azure.Commands.Network.Models.AzureApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="b57dc-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b57dc-126">NOTES</span></span>

## <span data-ttu-id="b57dc-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b57dc-127">RELATED LINKS</span></span>

[<span data-ttu-id="b57dc-128">Add-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="b57dc-128">Add-AzApplicationGatewayBackendHttpSetting</span></span>]()

[<span data-ttu-id="b57dc-129">New-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="b57dc-129">New-AzApplicationGatewayBackendHttpSetting</span></span>]()

[<span data-ttu-id="b57dc-130">Remove-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="b57dc-130">Remove-AzApplicationGatewayBackendHttpSetting</span></span>]()

[<span data-ttu-id="b57dc-131">Set-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="b57dc-131">Set-AzApplicationGatewayBackendHttpSetting</span></span>]()

