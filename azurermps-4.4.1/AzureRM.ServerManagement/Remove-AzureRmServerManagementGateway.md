---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: 41F8F851-6F9F-4DA4-8CE6-D8C9B7CF68D7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Remove-AzureRmServerManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Remove-AzureRmServerManagementGateway.md
ms.openlocfilehash: 2bcfac139d38f0b6f7d621a7761ce01d1d3f2f45
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577448"
---
# <span data-ttu-id="0ce68-101">Remove-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="0ce68-101">Remove-AzureRmServerManagementGateway</span></span>

## <span data-ttu-id="0ce68-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0ce68-102">SYNOPSIS</span></span>
<span data-ttu-id="0ce68-103">Tar bort en Server Management Gateway.</span><span class="sxs-lookup"><span data-stu-id="0ce68-103">Removes a Server Management gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0ce68-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0ce68-104">SYNTAX</span></span>

### <span data-ttu-id="0ce68-105">ByName</span><span class="sxs-lookup"><span data-stu-id="0ce68-105">ByName</span></span>
```
Remove-AzureRmServerManagementGateway [-ResourceGroupName] <String> [-GatewayName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0ce68-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="0ce68-106">ByObject</span></span>
```
Remove-AzureRmServerManagementGateway [-Gateway] <Gateway> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0ce68-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0ce68-107">DESCRIPTION</span></span>
<span data-ttu-id="0ce68-108">Cmdleten **Remove-AzureRmServerManagementGateway** tar bort en Azure Server Management Gateway.</span><span class="sxs-lookup"><span data-stu-id="0ce68-108">The **Remove-AzureRmServerManagementGateway** cmdlet removes an Azure Server Management gateway.</span></span>

## <span data-ttu-id="0ce68-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0ce68-109">EXAMPLES</span></span>

## <span data-ttu-id="0ce68-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0ce68-110">PARAMETERS</span></span>

### <span data-ttu-id="0ce68-111">-Gateway</span><span class="sxs-lookup"><span data-stu-id="0ce68-111">-Gateway</span></span>
<span data-ttu-id="0ce68-112">Anger den gateway som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="0ce68-112">Specifies the gateway that this cmdlet removes.</span></span>

<span data-ttu-id="0ce68-113">Denna parameter kan användas i stället för *ResourceGroupName* och *GatewayName* -parametrar.</span><span class="sxs-lookup"><span data-stu-id="0ce68-113">This parameter may be used instead of the *ResourceGroupName* and the *GatewayName* parameters.</span></span>

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

### <span data-ttu-id="0ce68-114">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="0ce68-114">-GatewayName</span></span>
<span data-ttu-id="0ce68-115">Anger namnet på den gateway som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="0ce68-115">Specifies the name of the gateway that this cmdlet removes.</span></span>

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

### <span data-ttu-id="0ce68-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ce68-116">-ResourceGroupName</span></span>
<span data-ttu-id="0ce68-117">Anger namnet på resurs gruppen som gatewayen tillhör.</span><span class="sxs-lookup"><span data-stu-id="0ce68-117">Specifies the name of the resource group in that the gateway belongs to.</span></span>

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

### <span data-ttu-id="0ce68-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ce68-118">-DefaultProfile</span></span>
<span data-ttu-id="0ce68-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0ce68-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0ce68-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ce68-120">CommonParameters</span></span>
<span data-ttu-id="0ce68-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ce68-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ce68-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ce68-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ce68-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0ce68-123">INPUTS</span></span>

### <span data-ttu-id="0ce68-124">Portar</span><span class="sxs-lookup"><span data-stu-id="0ce68-124">Gateway</span></span>
<span data-ttu-id="0ce68-125">Parameter "Gateway" accepterar värdet för typen Gateway från pipeline</span><span class="sxs-lookup"><span data-stu-id="0ce68-125">Parameter 'Gateway' accepts value of type 'Gateway' from the pipeline</span></span>

## <span data-ttu-id="0ce68-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0ce68-126">OUTPUTS</span></span>

## <span data-ttu-id="0ce68-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0ce68-127">NOTES</span></span>
* <span data-ttu-id="0ce68-128">Alla noder i gatewayen måste tas bort innan du använder denna cmdlet. i annat fall Miss lyckas denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0ce68-128">All the nodes in the Gateway must be removed before using this cmdlet; otherwise this cmdlet will fail.</span></span>

## <span data-ttu-id="0ce68-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0ce68-129">RELATED LINKS</span></span>

[<span data-ttu-id="0ce68-130">Get-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="0ce68-130">Get-AzureRmServerManagementGateway</span></span>](./Get-AzureRmServerManagementGateway.md)

[<span data-ttu-id="0ce68-131">New-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="0ce68-131">New-AzureRmServerManagementGateway</span></span>](./New-AzureRmServerManagementGateway.md)


