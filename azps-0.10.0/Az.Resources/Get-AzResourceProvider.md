---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6AB09621-488B-4A16-92D9-9C47EB87DA95
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azresourceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzResourceProvider.md
ms.openlocfilehash: cc890bf13922069ac9f4d20d6a9e8d0c3aa04c94
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923982"
---
# <span data-ttu-id="74de1-101">Get-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="74de1-101">Get-AzResourceProvider</span></span>

## <span data-ttu-id="74de1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="74de1-102">SYNOPSIS</span></span>
<span data-ttu-id="74de1-103">Får en resurs leverantör.</span><span class="sxs-lookup"><span data-stu-id="74de1-103">Gets a resource provider.</span></span>

## <span data-ttu-id="74de1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="74de1-104">SYNTAX</span></span>

### <span data-ttu-id="74de1-105">ListAvailable (standard)</span><span class="sxs-lookup"><span data-stu-id="74de1-105">ListAvailable (Default)</span></span>
```
Get-AzResourceProvider [-Location <String>] [-ListAvailable] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="74de1-106">IndividualProvider</span><span class="sxs-lookup"><span data-stu-id="74de1-106">IndividualProvider</span></span>
```
Get-AzResourceProvider -ProviderNamespace <String[]> [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="74de1-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="74de1-107">DESCRIPTION</span></span>
<span data-ttu-id="74de1-108">Cmdleten **Get-AzResourceProvider** får en Azure Resource-leverantör.</span><span class="sxs-lookup"><span data-stu-id="74de1-108">The **Get-AzResourceProvider** cmdlet gets an Azure resource provider.</span></span>

## <span data-ttu-id="74de1-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="74de1-109">EXAMPLES</span></span>

## <span data-ttu-id="74de1-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="74de1-110">PARAMETERS</span></span>

### <span data-ttu-id="74de1-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="74de1-111">-ApiVersion</span></span>
<span data-ttu-id="74de1-112">Anger den API-version som stöds av resurs leverantören.</span><span class="sxs-lookup"><span data-stu-id="74de1-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="74de1-113">Du kan ange en annan version än standard versionen.</span><span class="sxs-lookup"><span data-stu-id="74de1-113">You can specify a different version than the default version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74de1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74de1-114">-DefaultProfile</span></span>
<span data-ttu-id="74de1-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="74de1-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74de1-116">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="74de1-116">-ListAvailable</span></span>
<span data-ttu-id="74de1-117">Indikerar att den här åtgärden får alla tillgängliga resurs leverantörer.</span><span class="sxs-lookup"><span data-stu-id="74de1-117">Indicates that this operation gets all available resource providers.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListAvailable
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74de1-118">-Plats</span><span class="sxs-lookup"><span data-stu-id="74de1-118">-Location</span></span>
<span data-ttu-id="74de1-119">Anger resurs leverantörens plats.</span><span class="sxs-lookup"><span data-stu-id="74de1-119">Specifies the location of the resource provider.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74de1-120">-För</span><span class="sxs-lookup"><span data-stu-id="74de1-120">-Pre</span></span>
<span data-ttu-id="74de1-121">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="74de1-121">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="74de1-122">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="74de1-122">-ProviderNamespace</span></span>
<span data-ttu-id="74de1-123">Anger resurs leverantörens namn område.</span><span class="sxs-lookup"><span data-stu-id="74de1-123">Specifies the namespace of the resource provider.</span></span>

```yaml
Type: System.String[]
Parameter Sets: IndividualProvider
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74de1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74de1-124">CommonParameters</span></span>
<span data-ttu-id="74de1-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74de1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74de1-126">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74de1-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74de1-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="74de1-127">INPUTS</span></span>

## <span data-ttu-id="74de1-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="74de1-128">OUTPUTS</span></span>

## <span data-ttu-id="74de1-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="74de1-129">NOTES</span></span>

## <span data-ttu-id="74de1-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="74de1-130">RELATED LINKS</span></span>

[<span data-ttu-id="74de1-131">Register-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="74de1-131">Register-AzResourceProvider</span></span>](./Register-AzResourceProvider.md)

[<span data-ttu-id="74de1-132">Avregistrera-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="74de1-132">Unregister-AzResourceProvider</span></span>](./Unregister-AzResourceProvider.md)


