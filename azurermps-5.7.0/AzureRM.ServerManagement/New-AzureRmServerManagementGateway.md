---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: D7485CB9-AE12-445B-8984-3D21FCA0E82F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servermanagement/new-azurermservermanagementgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementGateway.md
ms.openlocfilehash: f73d53fc3031fc72be950547e5b9c2b93a9a0079
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755588"
---
# <span data-ttu-id="c089d-101">New-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="c089d-101">New-AzureRmServerManagementGateway</span></span>

## <span data-ttu-id="c089d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c089d-102">SYNOPSIS</span></span>
<span data-ttu-id="c089d-103">Skapar en server hanterings-Gateway.</span><span class="sxs-lookup"><span data-stu-id="c089d-103">Creates a Server Management gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c089d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c089d-104">SYNTAX</span></span>

```
New-AzureRmServerManagementGateway [-ResourceGroupName] <String> [-GatewayName] <String> [-Location] <String>
 [-AutoUpgrade] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c089d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c089d-105">DESCRIPTION</span></span>
<span data-ttu-id="c089d-106">Cmdleten **New-AzureRmServerManagementGateway** skapar en Azure Server Management Gateway.</span><span class="sxs-lookup"><span data-stu-id="c089d-106">The **New-AzureRmServerManagementGateway** cmdlet creates an Azure Server Management gateway.</span></span>

## <span data-ttu-id="c089d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c089d-107">EXAMPLES</span></span>

## <span data-ttu-id="c089d-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c089d-108">PARAMETERS</span></span>

### <span data-ttu-id="c089d-109">-Autouppgradering</span><span class="sxs-lookup"><span data-stu-id="c089d-109">-AutoUpgrade</span></span>
<span data-ttu-id="c089d-110">Anger att gatewayen automatiskt uppgraderas när en ny version släpps.</span><span class="sxs-lookup"><span data-stu-id="c089d-110">Indicates that the gateway will auto upgrade itself when a new version is released.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c089d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c089d-111">-DefaultProfile</span></span>
<span data-ttu-id="c089d-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c089d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c089d-113">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="c089d-113">-GatewayName</span></span>
<span data-ttu-id="c089d-114">Anger namnet på den gateway som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="c089d-114">Specifies the name of the gateway that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c089d-115">-Plats</span><span class="sxs-lookup"><span data-stu-id="c089d-115">-Location</span></span>
<span data-ttu-id="c089d-116">Anger den plats där du vill skapa gatewayen.</span><span class="sxs-lookup"><span data-stu-id="c089d-116">Specifies the location in which to create the gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c089d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c089d-117">-ResourceGroupName</span></span>
<span data-ttu-id="c089d-118">Anger namnet på resurs gruppen där denna cmdlet skapar gatewayen.</span><span class="sxs-lookup"><span data-stu-id="c089d-118">Specifies the name of the resource group in which this cmdlet creates the gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c089d-119">-Tagg</span><span class="sxs-lookup"><span data-stu-id="c089d-119">-Tag</span></span>
<span data-ttu-id="c089d-120">Nyckelord som är kopplade till gatewayen.</span><span class="sxs-lookup"><span data-stu-id="c089d-120">Key/value pairs associated with the gateway.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c089d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c089d-121">CommonParameters</span></span>
<span data-ttu-id="c089d-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c089d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c089d-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c089d-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c089d-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c089d-124">INPUTS</span></span>

### <span data-ttu-id="c089d-125">Ingen</span><span class="sxs-lookup"><span data-stu-id="c089d-125">None</span></span>
<span data-ttu-id="c089d-126">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="c089d-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c089d-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c089d-127">OUTPUTS</span></span>

### <span data-ttu-id="c089d-128">Microsoft. Azure. commands. ServerManagement. Model. Gateway</span><span class="sxs-lookup"><span data-stu-id="c089d-128">Microsoft.Azure.Commands.ServerManagement.Model.Gateway</span></span>

## <span data-ttu-id="c089d-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c089d-129">NOTES</span></span>

## <span data-ttu-id="c089d-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c089d-130">RELATED LINKS</span></span>

[<span data-ttu-id="c089d-131">Get-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="c089d-131">Get-AzureRmServerManagementGateway</span></span>](./Get-AzureRmServerManagementGateway.md)

[<span data-ttu-id="c089d-132">Remove-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="c089d-132">Remove-AzureRmServerManagementGateway</span></span>](./Remove-AzureRmServerManagementGateway.md)


