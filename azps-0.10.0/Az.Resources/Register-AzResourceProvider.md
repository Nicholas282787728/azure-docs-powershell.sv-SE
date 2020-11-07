---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D5067FD8-2FB1-413C-9F59-84E83A74343E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/register-Azresourceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Register-AzResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Register-AzResourceProvider.md
ms.openlocfilehash: 7f9a5089e48da7c49716abe2bdbe710c0cf30e3b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923878"
---
# <span data-ttu-id="82a6a-101">Register-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="82a6a-101">Register-AzResourceProvider</span></span>

## <span data-ttu-id="82a6a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="82a6a-102">SYNOPSIS</span></span>
<span data-ttu-id="82a6a-103">Registrerar en resurs leverantör.</span><span class="sxs-lookup"><span data-stu-id="82a6a-103">Registers a resource provider.</span></span>

## <span data-ttu-id="82a6a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="82a6a-104">SYNTAX</span></span>

```
Register-AzResourceProvider -ProviderNamespace <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82a6a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="82a6a-105">DESCRIPTION</span></span>
<span data-ttu-id="82a6a-106">**Register-AzResourceProvider** cmdlet registrerar en Azure Resource-leverantör.</span><span class="sxs-lookup"><span data-stu-id="82a6a-106">The **Register-AzResourceProvider** cmdlet registers an Azure resource provider.</span></span>

## <span data-ttu-id="82a6a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="82a6a-107">EXAMPLES</span></span>

### <span data-ttu-id="82a6a-108">Exempel 1: registrera en leverantör</span><span class="sxs-lookup"><span data-stu-id="82a6a-108">Example 1: Register a provider</span></span>
```
PS C:\>Register-AzResourceProvider -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="82a6a-109">Detta registrerar Microsoft. Network-leverantören för ditt konto.</span><span class="sxs-lookup"><span data-stu-id="82a6a-109">This registers the Microsoft.Network provider for your account.</span></span>

## <span data-ttu-id="82a6a-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="82a6a-110">PARAMETERS</span></span>

### <span data-ttu-id="82a6a-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="82a6a-111">-ApiVersion</span></span>
<span data-ttu-id="82a6a-112">Anger den API-version som stöds av resurs leverantören.</span><span class="sxs-lookup"><span data-stu-id="82a6a-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="82a6a-113">Du kan ange en annan version än standard versionen.</span><span class="sxs-lookup"><span data-stu-id="82a6a-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="82a6a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82a6a-114">-DefaultProfile</span></span>
<span data-ttu-id="82a6a-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="82a6a-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="82a6a-116">-För</span><span class="sxs-lookup"><span data-stu-id="82a6a-116">-Pre</span></span>
<span data-ttu-id="82a6a-117">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="82a6a-117">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="82a6a-118">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="82a6a-118">-ProviderNamespace</span></span>
<span data-ttu-id="82a6a-119">Anger resurs leverantörens namn område.</span><span class="sxs-lookup"><span data-stu-id="82a6a-119">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="82a6a-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="82a6a-120">-Confirm</span></span>
<span data-ttu-id="82a6a-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="82a6a-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82a6a-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82a6a-122">-WhatIf</span></span>
<span data-ttu-id="82a6a-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="82a6a-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82a6a-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="82a6a-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82a6a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82a6a-125">CommonParameters</span></span>
<span data-ttu-id="82a6a-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82a6a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82a6a-127">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82a6a-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82a6a-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="82a6a-128">INPUTS</span></span>

## <span data-ttu-id="82a6a-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="82a6a-129">OUTPUTS</span></span>

## <span data-ttu-id="82a6a-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="82a6a-130">NOTES</span></span>

## <span data-ttu-id="82a6a-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="82a6a-131">RELATED LINKS</span></span>

[<span data-ttu-id="82a6a-132">Get-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="82a6a-132">Get-AzResourceProvider</span></span>](./Get-AzResourceProvider.md)

[<span data-ttu-id="82a6a-133">Avregistrera-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="82a6a-133">Unregister-AzResourceProvider</span></span>](./Unregister-AzResourceProvider.md)


