---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D5126B7B-7FBB-4C72-B77E-13ADE2BE9B1B
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/unregister-azresourceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Unregister-AzResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Unregister-AzResourceProvider.md
ms.openlocfilehash: be32315e62770de7075f89fc1390063d4c516211
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98401147"
---
# <span data-ttu-id="32fb3-101">Unregister-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="32fb3-101">Unregister-AzResourceProvider</span></span>

## <span data-ttu-id="32fb3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="32fb3-102">SYNOPSIS</span></span>
<span data-ttu-id="32fb3-103">Avregistrerar en resurs leverantör.</span><span class="sxs-lookup"><span data-stu-id="32fb3-103">Unregisters a resource provider.</span></span>

## <span data-ttu-id="32fb3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="32fb3-104">SYNTAX</span></span>

```
Unregister-AzResourceProvider -ProviderNamespace <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32fb3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="32fb3-105">DESCRIPTION</span></span>
<span data-ttu-id="32fb3-106">Med cmdleten **Unregistered-AzResourceProvider** avregistrerar du en Azure-resurs.</span><span class="sxs-lookup"><span data-stu-id="32fb3-106">The **Unregister-AzResourceProvider** cmdlet unregisters an Azure resource provider.</span></span>

## <span data-ttu-id="32fb3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="32fb3-107">EXAMPLES</span></span>

### <span data-ttu-id="32fb3-108">Exempel 1: avregistrera resurs leverantör med ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="32fb3-108">Example 1: Unregister resource provider with ProviderNamespace</span></span>

```powershell
PS C:\>Unregister-AzResourceProvider -ProviderNamespace "Microsoft.support"
```

<span data-ttu-id="32fb3-109">Det här kommandot avregistrerar resurs leverantören "Microsoft. support".</span><span class="sxs-lookup"><span data-stu-id="32fb3-109">This command unregisters the resource provider "Microsoft.support".</span></span>

## <span data-ttu-id="32fb3-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="32fb3-110">PARAMETERS</span></span>

### <span data-ttu-id="32fb3-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="32fb3-111">-ApiVersion</span></span>
<span data-ttu-id="32fb3-112">Anger den API-version som stöds av resurs leverantören.</span><span class="sxs-lookup"><span data-stu-id="32fb3-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="32fb3-113">Du kan ange en annan version än standard versionen.</span><span class="sxs-lookup"><span data-stu-id="32fb3-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="32fb3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32fb3-114">-DefaultProfile</span></span>
<span data-ttu-id="32fb3-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="32fb3-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="32fb3-116">-För</span><span class="sxs-lookup"><span data-stu-id="32fb3-116">-Pre</span></span>
<span data-ttu-id="32fb3-117">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="32fb3-117">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="32fb3-118">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="32fb3-118">-ProviderNamespace</span></span>
<span data-ttu-id="32fb3-119">Anger resurs leverantörens namn område.</span><span class="sxs-lookup"><span data-stu-id="32fb3-119">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="32fb3-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="32fb3-120">-Confirm</span></span>
<span data-ttu-id="32fb3-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="32fb3-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32fb3-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32fb3-122">-WhatIf</span></span>
<span data-ttu-id="32fb3-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="32fb3-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32fb3-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="32fb3-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32fb3-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32fb3-125">CommonParameters</span></span>
<span data-ttu-id="32fb3-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32fb3-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32fb3-127">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="32fb3-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32fb3-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="32fb3-128">INPUTS</span></span>

### <span data-ttu-id="32fb3-129">System. String</span><span class="sxs-lookup"><span data-stu-id="32fb3-129">System.String</span></span>

## <span data-ttu-id="32fb3-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="32fb3-130">OUTPUTS</span></span>

### <span data-ttu-id="32fb3-131">Microsoft. Azure. kommandon. ResourceManager. cmdlets. SdkModels. PSResourceProvider</span><span class="sxs-lookup"><span data-stu-id="32fb3-131">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span></span>

## <span data-ttu-id="32fb3-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="32fb3-132">NOTES</span></span>

## <span data-ttu-id="32fb3-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="32fb3-133">RELATED LINKS</span></span>

[<span data-ttu-id="32fb3-134">Get-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="32fb3-134">Get-AzResourceProvider</span></span>](./Get-AzResourceProvider.md)

[<span data-ttu-id="32fb3-135">Register-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="32fb3-135">Register-AzResourceProvider</span></span>](./Register-AzResourceProvider.md)


