---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 91919242-59ED-4938-A3A3-23A66F85FBC1
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOrigin.md
ms.openlocfilehash: e5e27dba4519d16ebc304f3d6cca99f32f23e341
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94272767"
---
# <span data-ttu-id="16ecd-101">Get-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="16ecd-101">Get-AzCdnOrigin</span></span>

## <span data-ttu-id="16ecd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="16ecd-102">SYNOPSIS</span></span>
<span data-ttu-id="16ecd-103">Hämtar en CDN Origin Server.</span><span class="sxs-lookup"><span data-stu-id="16ecd-103">Gets a CDN origin server.</span></span>

## <span data-ttu-id="16ecd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="16ecd-104">SYNTAX</span></span>

### <span data-ttu-id="16ecd-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="16ecd-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnOrigin [-OriginName <String>] -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="16ecd-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="16ecd-106">ByResourceIdParameterSet</span></span>
```
Get-AzCdnOrigin [-OriginName <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="16ecd-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="16ecd-107">ByObjectParameterSet</span></span>
```
Get-AzCdnOrigin [-OriginName <String>] -CdnEndpoint <PSEndpoint> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="16ecd-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="16ecd-108">DESCRIPTION</span></span>
<span data-ttu-id="16ecd-109">Cmdleten **Get-AzCdnOrigin** hämtar en Origine-Server och dess konfigurations data.</span><span class="sxs-lookup"><span data-stu-id="16ecd-109">The **Get-AzCdnOrigin** cmdlet gets an Azure Content Delivery Network (CDN) origin server and its configuration data.</span></span>

## <span data-ttu-id="16ecd-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="16ecd-110">EXAMPLES</span></span>

## <span data-ttu-id="16ecd-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="16ecd-111">PARAMETERS</span></span>

### <span data-ttu-id="16ecd-112">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="16ecd-112">-CdnEndpoint</span></span>
<span data-ttu-id="16ecd-113">Anger det CDN-slutobjekt som ursprunget tillhör.</span><span class="sxs-lookup"><span data-stu-id="16ecd-113">Specifies the CDN endpoint object to which the origin belongs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="16ecd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16ecd-114">-DefaultProfile</span></span>
<span data-ttu-id="16ecd-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="16ecd-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="16ecd-116">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="16ecd-116">-EndpointName</span></span>
<span data-ttu-id="16ecd-117">Anger namnet på den slut punkt som ursprungs servern tillhör.</span><span class="sxs-lookup"><span data-stu-id="16ecd-117">Specifies the name of the endpoint to which the origin server belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16ecd-118">-OriginName</span><span class="sxs-lookup"><span data-stu-id="16ecd-118">-OriginName</span></span>
<span data-ttu-id="16ecd-119">Anger namnet på ursprungs servern.</span><span class="sxs-lookup"><span data-stu-id="16ecd-119">Specifies the name of the origin server.</span></span>

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

### <span data-ttu-id="16ecd-120">-Profilnamn</span><span class="sxs-lookup"><span data-stu-id="16ecd-120">-ProfileName</span></span>
<span data-ttu-id="16ecd-121">Anger namnet på den profil som ursprungs servern tillhör.</span><span class="sxs-lookup"><span data-stu-id="16ecd-121">Specifies the name of the profile to which the origin server belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16ecd-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16ecd-122">-ResourceGroupName</span></span>
<span data-ttu-id="16ecd-123">Anger namnet på den resurs grupp som ursprungs servern tillhör.</span><span class="sxs-lookup"><span data-stu-id="16ecd-123">Specifies the name of the resource group to which the origin server belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16ecd-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="16ecd-124">-ResourceId</span></span>
<span data-ttu-id="16ecd-125">Resurs-ID för Azure CDN-ursprung.</span><span class="sxs-lookup"><span data-stu-id="16ecd-125">The resource id of the Azure CDN origin.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16ecd-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16ecd-126">CommonParameters</span></span>
<span data-ttu-id="16ecd-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16ecd-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16ecd-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="16ecd-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16ecd-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="16ecd-129">INPUTS</span></span>

### <span data-ttu-id="16ecd-130">Microsoft. Azure. commands. CDN. Models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="16ecd-130">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="16ecd-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="16ecd-131">OUTPUTS</span></span>

### <span data-ttu-id="16ecd-132">Microsoft. Azure. commands. CDN. Models. ORIGIN. PSOrigin</span><span class="sxs-lookup"><span data-stu-id="16ecd-132">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="16ecd-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="16ecd-133">NOTES</span></span>

## <span data-ttu-id="16ecd-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="16ecd-134">RELATED LINKS</span></span>

[<span data-ttu-id="16ecd-135">Set-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="16ecd-135">Set-AzCdnOrigin</span></span>](./Set-AzCdnOrigin.md)


