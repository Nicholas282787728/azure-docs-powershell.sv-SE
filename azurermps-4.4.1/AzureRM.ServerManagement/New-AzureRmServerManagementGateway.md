---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: D7485CB9-AE12-445B-8984-3D21FCA0E82F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementGateway.md
ms.openlocfilehash: 9cb98b9671f43ddd7acbcc84e8473a12da00f405
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577452"
---
# <span data-ttu-id="ac789-101">New-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="ac789-101">New-AzureRmServerManagementGateway</span></span>

## <span data-ttu-id="ac789-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ac789-102">SYNOPSIS</span></span>
<span data-ttu-id="ac789-103">Skapar en server hanterings-Gateway.</span><span class="sxs-lookup"><span data-stu-id="ac789-103">Creates a Server Management gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ac789-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ac789-104">SYNTAX</span></span>

```
New-AzureRmServerManagementGateway [-ResourceGroupName] <String> [-GatewayName] <String> [-Location] <String>
 [-AutoUpgrade] [-Tags <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ac789-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ac789-105">DESCRIPTION</span></span>
<span data-ttu-id="ac789-106">Cmdleten **New-AzureRmServerManagementGateway** skapar en Azure Server Management Gateway.</span><span class="sxs-lookup"><span data-stu-id="ac789-106">The **New-AzureRmServerManagementGateway** cmdlet creates an Azure Server Management gateway.</span></span>

## <span data-ttu-id="ac789-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ac789-107">EXAMPLES</span></span>

## <span data-ttu-id="ac789-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ac789-108">PARAMETERS</span></span>

### <span data-ttu-id="ac789-109">-Autouppgradering</span><span class="sxs-lookup"><span data-stu-id="ac789-109">-AutoUpgrade</span></span>
<span data-ttu-id="ac789-110">Anger att gatewayen automatiskt uppgraderas när en ny version släpps.</span><span class="sxs-lookup"><span data-stu-id="ac789-110">Indicates that the gateway will auto upgrade itself when a new version is released.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac789-111">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="ac789-111">-GatewayName</span></span>
<span data-ttu-id="ac789-112">Anger namnet på den gateway som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="ac789-112">Specifies the name of the gateway that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac789-113">-Plats</span><span class="sxs-lookup"><span data-stu-id="ac789-113">-Location</span></span>
<span data-ttu-id="ac789-114">Anger den plats där du vill skapa gatewayen.</span><span class="sxs-lookup"><span data-stu-id="ac789-114">Specifies the location in which to create the gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac789-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac789-115">-ResourceGroupName</span></span>
<span data-ttu-id="ac789-116">Anger namnet på resurs gruppen där denna cmdlet skapar gatewayen.</span><span class="sxs-lookup"><span data-stu-id="ac789-116">Specifies the name of the resource group in which this cmdlet creates the gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac789-117">-Taggar</span><span class="sxs-lookup"><span data-stu-id="ac789-117">-Tags</span></span>
<span data-ttu-id="ac789-118">Anger taggar som par med nyckelord.</span><span class="sxs-lookup"><span data-stu-id="ac789-118">Specifies tags as key-value pairs.</span></span>
<span data-ttu-id="ac789-119">Du kan använda taggar för att identifiera en gateway från andra Azure-resurser.</span><span class="sxs-lookup"><span data-stu-id="ac789-119">You can use tags to identify a Gateway from other Azure resources.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac789-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac789-120">-DefaultProfile</span></span>
<span data-ttu-id="ac789-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ac789-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ac789-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac789-122">CommonParameters</span></span>
<span data-ttu-id="ac789-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac789-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac789-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac789-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac789-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ac789-125">INPUTS</span></span>

## <span data-ttu-id="ac789-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ac789-126">OUTPUTS</span></span>

### <span data-ttu-id="ac789-127">Microsoft. Azure. commands. ServerManagement. Model. Gateway</span><span class="sxs-lookup"><span data-stu-id="ac789-127">Microsoft.Azure.Commands.ServerManagement.Model.Gateway</span></span>

## <span data-ttu-id="ac789-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ac789-128">NOTES</span></span>

## <span data-ttu-id="ac789-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ac789-129">RELATED LINKS</span></span>

[<span data-ttu-id="ac789-130">Get-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="ac789-130">Get-AzureRmServerManagementGateway</span></span>](./Get-AzureRmServerManagementGateway.md)

[<span data-ttu-id="ac789-131">Remove-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="ac789-131">Remove-AzureRmServerManagementGateway</span></span>](./Remove-AzureRmServerManagementGateway.md)


