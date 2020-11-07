---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: 22B63259-799B-4F25-A06B-7A818D295870
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Reset-AzureRmServerManagementGatewayProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Reset-AzureRmServerManagementGatewayProfile.md
ms.openlocfilehash: 9ce8dc1faf1a762a847da5eb87fb28b510308054
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756548"
---
# <span data-ttu-id="df3f4-101">Reset-AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="df3f4-101">Reset-AzureRmServerManagementGatewayProfile</span></span>

## <span data-ttu-id="df3f4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="df3f4-102">SYNOPSIS</span></span>
<span data-ttu-id="df3f4-103">Återställer profilen för en server hanterings-Gateway.</span><span class="sxs-lookup"><span data-stu-id="df3f4-103">Resets the profile of a Server Management gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="df3f4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="df3f4-104">SYNTAX</span></span>

### <span data-ttu-id="df3f4-105">ByName</span><span class="sxs-lookup"><span data-stu-id="df3f4-105">ByName</span></span>
```
Reset-AzureRmServerManagementGatewayProfile [-ResourceGroupName] <String> [-GatewayName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="df3f4-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="df3f4-106">ByObject</span></span>
```
Reset-AzureRmServerManagementGatewayProfile [-Gateway] <Gateway> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="df3f4-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="df3f4-107">DESCRIPTION</span></span>
<span data-ttu-id="df3f4-108">Cmdleten **Reset-AzureRmServerManagementGatewayProfile** återställer profilen för en Azure Server Management Gateway.</span><span class="sxs-lookup"><span data-stu-id="df3f4-108">The **Reset-AzureRmServerManagementGatewayProfile** cmdlet resets the profile for an Azure Server Management Gateway.</span></span>

<span data-ttu-id="df3f4-109">Du måste använda Save-AzureRmServerManagementGatewayProfile cmdlet för att hämta profilen och sedan Install-AzureRmServerManagementGatewayProfile cmdlet för att spara den när du har återställt profilen.</span><span class="sxs-lookup"><span data-stu-id="df3f4-109">You will need to use the Save-AzureRmServerManagementGatewayProfile cmdlet to download the profile and then the Install-AzureRmServerManagementGatewayProfile cmdlet to save it after you reset the profile.</span></span>

## <span data-ttu-id="df3f4-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="df3f4-110">EXAMPLES</span></span>

## <span data-ttu-id="df3f4-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="df3f4-111">PARAMETERS</span></span>

### <span data-ttu-id="df3f4-112">-Gateway</span><span class="sxs-lookup"><span data-stu-id="df3f4-112">-Gateway</span></span>
<span data-ttu-id="df3f4-113">Anger den gateway för vilken cmdleten återställer profilen för.</span><span class="sxs-lookup"><span data-stu-id="df3f4-113">Specifies the gateway for which the cmdlet resets the profile for.</span></span>

<span data-ttu-id="df3f4-114">Kan anges i stället för ResourceGoupName och GatewayName</span><span class="sxs-lookup"><span data-stu-id="df3f4-114">May be specified instead of ResourceGoupName and GatewayName</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServerManagement.Model.Gateway
Parameter Sets: ByObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="df3f4-115">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="df3f4-115">-GatewayName</span></span>
<span data-ttu-id="df3f4-116">Anger namnet på den gateway där cmdleten återställer profilen.</span><span class="sxs-lookup"><span data-stu-id="df3f4-116">Specifies the name of the gateway for which the cmdlet resets the profile.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df3f4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df3f4-117">-ResourceGroupName</span></span>
<span data-ttu-id="df3f4-118">Anger namnet på resurs gruppen som gatewayen tillhör.</span><span class="sxs-lookup"><span data-stu-id="df3f4-118">Specifies the name of the resource group that the gateway belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df3f4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df3f4-119">-DefaultProfile</span></span>
<span data-ttu-id="df3f4-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="df3f4-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df3f4-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df3f4-121">CommonParameters</span></span>
<span data-ttu-id="df3f4-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df3f4-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df3f4-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df3f4-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df3f4-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="df3f4-124">INPUTS</span></span>

### <span data-ttu-id="df3f4-125">Portar</span><span class="sxs-lookup"><span data-stu-id="df3f4-125">Gateway</span></span>
<span data-ttu-id="df3f4-126">Parameter "Gateway" accepterar värdet för typen Gateway från pipeline</span><span class="sxs-lookup"><span data-stu-id="df3f4-126">Parameter 'Gateway' accepts value of type 'Gateway' from the pipeline</span></span>

## <span data-ttu-id="df3f4-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="df3f4-127">OUTPUTS</span></span>

## <span data-ttu-id="df3f4-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="df3f4-128">NOTES</span></span>

## <span data-ttu-id="df3f4-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="df3f4-129">RELATED LINKS</span></span>

[<span data-ttu-id="df3f4-130">Install-AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="df3f4-130">Install-AzureRmServerManagementGatewayProfile</span></span>](./Install-AzureRmServerManagementGatewayProfile.md)

[<span data-ttu-id="df3f4-131">Spara – AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="df3f4-131">Save-AzureRmServerManagementGatewayProfile</span></span>](./Save-AzureRmServerManagementGatewayProfile.md)


