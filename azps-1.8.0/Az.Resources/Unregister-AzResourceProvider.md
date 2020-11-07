---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D5126B7B-7FBB-4C72-B77E-13ADE2BE9B1B
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/unregister-azresourceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Unregister-AzResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Unregister-AzResourceProvider.md
ms.openlocfilehash: de2a213122f756d87255be6195759e467f64b428
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747020"
---
# <span data-ttu-id="00440-101">Unregister-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="00440-101">Unregister-AzResourceProvider</span></span>

## <span data-ttu-id="00440-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="00440-102">SYNOPSIS</span></span>
<span data-ttu-id="00440-103">Avregistrerar en resurs leverantör.</span><span class="sxs-lookup"><span data-stu-id="00440-103">Unregisters a resource provider.</span></span>

## <span data-ttu-id="00440-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="00440-104">SYNTAX</span></span>

```
Unregister-AzResourceProvider -ProviderNamespace <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="00440-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="00440-105">DESCRIPTION</span></span>
<span data-ttu-id="00440-106">Med cmdleten **Unregistered-AzResourceProvider** avregistrerar du en Azure-resurs.</span><span class="sxs-lookup"><span data-stu-id="00440-106">The **Unregister-AzResourceProvider** cmdlet unregisters an Azure resource provider.</span></span>

## <span data-ttu-id="00440-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="00440-107">EXAMPLES</span></span>

## <span data-ttu-id="00440-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="00440-108">PARAMETERS</span></span>

### <span data-ttu-id="00440-109">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="00440-109">-ApiVersion</span></span>
<span data-ttu-id="00440-110">Anger den API-version som stöds av resurs leverantören.</span><span class="sxs-lookup"><span data-stu-id="00440-110">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="00440-111">Du kan ange en annan version än standard versionen.</span><span class="sxs-lookup"><span data-stu-id="00440-111">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="00440-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00440-112">-DefaultProfile</span></span>
<span data-ttu-id="00440-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="00440-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="00440-114">-För</span><span class="sxs-lookup"><span data-stu-id="00440-114">-Pre</span></span>
<span data-ttu-id="00440-115">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="00440-115">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="00440-116">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="00440-116">-ProviderNamespace</span></span>
<span data-ttu-id="00440-117">Anger resurs leverantörens namn område.</span><span class="sxs-lookup"><span data-stu-id="00440-117">Specifies the namespace of the resource provider.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00440-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="00440-118">-Confirm</span></span>
<span data-ttu-id="00440-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="00440-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00440-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00440-120">-WhatIf</span></span>
<span data-ttu-id="00440-121">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="00440-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00440-122">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="00440-122">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00440-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00440-123">CommonParameters</span></span>
<span data-ttu-id="00440-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00440-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00440-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00440-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00440-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="00440-126">INPUTS</span></span>

### <span data-ttu-id="00440-127">System. String</span><span class="sxs-lookup"><span data-stu-id="00440-127">System.String</span></span>

## <span data-ttu-id="00440-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="00440-128">OUTPUTS</span></span>

### <span data-ttu-id="00440-129">Microsoft. Azure. kommandon. ResourceManager. cmdlets. SdkModels. PSResourceProvider</span><span class="sxs-lookup"><span data-stu-id="00440-129">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span></span>

## <span data-ttu-id="00440-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="00440-130">NOTES</span></span>

## <span data-ttu-id="00440-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="00440-131">RELATED LINKS</span></span>

[<span data-ttu-id="00440-132">Get-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="00440-132">Get-AzResourceProvider</span></span>](./Get-AzResourceProvider.md)

[<span data-ttu-id="00440-133">Register-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="00440-133">Register-AzResourceProvider</span></span>](./Register-AzResourceProvider.md)


