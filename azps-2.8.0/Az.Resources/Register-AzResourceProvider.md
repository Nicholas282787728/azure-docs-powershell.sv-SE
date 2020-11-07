---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D5067FD8-2FB1-413C-9F59-84E83A74343E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/register-azresourceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Register-AzResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Register-AzResourceProvider.md
ms.openlocfilehash: 11ff763dacc5a6969501dae925fbbc2382c871b3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920064"
---
# <span data-ttu-id="1fd5e-101">Register-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="1fd5e-101">Register-AzResourceProvider</span></span>

## <span data-ttu-id="1fd5e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1fd5e-102">SYNOPSIS</span></span>
<span data-ttu-id="1fd5e-103">Registrerar en resurs leverantör.</span><span class="sxs-lookup"><span data-stu-id="1fd5e-103">Registers a resource provider.</span></span>

## <span data-ttu-id="1fd5e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1fd5e-104">SYNTAX</span></span>

```
Register-AzResourceProvider -ProviderNamespace <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1fd5e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1fd5e-105">DESCRIPTION</span></span>
<span data-ttu-id="1fd5e-106">**Register-AzResourceProvider** cmdlet registrerar en Azure Resource-leverantör.</span><span class="sxs-lookup"><span data-stu-id="1fd5e-106">The **Register-AzResourceProvider** cmdlet registers an Azure resource provider.</span></span>

## <span data-ttu-id="1fd5e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1fd5e-107">EXAMPLES</span></span>

### <span data-ttu-id="1fd5e-108">Exempel 1: registrera en leverantör</span><span class="sxs-lookup"><span data-stu-id="1fd5e-108">Example 1: Register a provider</span></span>
```
PS C:\>Register-AzResourceProvider -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="1fd5e-109">Detta registrerar Microsoft. Network-leverantören för ditt konto.</span><span class="sxs-lookup"><span data-stu-id="1fd5e-109">This registers the Microsoft.Network provider for your account.</span></span>

## <span data-ttu-id="1fd5e-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1fd5e-110">PARAMETERS</span></span>

### <span data-ttu-id="1fd5e-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="1fd5e-111">-ApiVersion</span></span>
<span data-ttu-id="1fd5e-112">Anger den API-version som stöds av resurs leverantören.</span><span class="sxs-lookup"><span data-stu-id="1fd5e-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="1fd5e-113">Du kan ange en annan version än standard versionen.</span><span class="sxs-lookup"><span data-stu-id="1fd5e-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="1fd5e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fd5e-114">-DefaultProfile</span></span>
<span data-ttu-id="1fd5e-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="1fd5e-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1fd5e-116">-För</span><span class="sxs-lookup"><span data-stu-id="1fd5e-116">-Pre</span></span>
<span data-ttu-id="1fd5e-117">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="1fd5e-117">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="1fd5e-118">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="1fd5e-118">-ProviderNamespace</span></span>
<span data-ttu-id="1fd5e-119">Anger resurs leverantörens namn område.</span><span class="sxs-lookup"><span data-stu-id="1fd5e-119">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="1fd5e-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1fd5e-120">-Confirm</span></span>
<span data-ttu-id="1fd5e-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1fd5e-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1fd5e-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1fd5e-122">-WhatIf</span></span>
<span data-ttu-id="1fd5e-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1fd5e-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1fd5e-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1fd5e-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1fd5e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fd5e-125">CommonParameters</span></span>
<span data-ttu-id="1fd5e-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1fd5e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fd5e-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1fd5e-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fd5e-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1fd5e-128">INPUTS</span></span>

### <span data-ttu-id="1fd5e-129">System. String</span><span class="sxs-lookup"><span data-stu-id="1fd5e-129">System.String</span></span>

## <span data-ttu-id="1fd5e-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1fd5e-130">OUTPUTS</span></span>

### <span data-ttu-id="1fd5e-131">Microsoft. Azure. kommandon. ResourceManager. cmdlets. SdkModels. PSResourceProvider</span><span class="sxs-lookup"><span data-stu-id="1fd5e-131">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span></span>

## <span data-ttu-id="1fd5e-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1fd5e-132">NOTES</span></span>

## <span data-ttu-id="1fd5e-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1fd5e-133">RELATED LINKS</span></span>

[<span data-ttu-id="1fd5e-134">Get-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="1fd5e-134">Get-AzResourceProvider</span></span>](./Get-AzResourceProvider.md)

[<span data-ttu-id="1fd5e-135">Avregistrera-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="1fd5e-135">Unregister-AzResourceProvider</span></span>](./Unregister-AzResourceProvider.md)


