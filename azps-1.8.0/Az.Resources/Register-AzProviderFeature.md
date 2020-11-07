---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 83EE33E5-18EF-4A7A-AEF2-E93D7A3CA541
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/register-azproviderfeature
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Register-AzProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Register-AzProviderFeature.md
ms.openlocfilehash: 57a01f831ab92b7ae8ca45fbf9535ed4fa7df0a1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747099"
---
# <span data-ttu-id="d96af-101">Register-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="d96af-101">Register-AzProviderFeature</span></span>

## <span data-ttu-id="d96af-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d96af-102">SYNOPSIS</span></span>
<span data-ttu-id="d96af-103">Registrerar en Azure-leverantör i ditt konto.</span><span class="sxs-lookup"><span data-stu-id="d96af-103">Registers an Azure provider feature in your account.</span></span>

## <span data-ttu-id="d96af-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d96af-104">SYNTAX</span></span>

```
Register-AzProviderFeature -FeatureName <String> -ProviderNamespace <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d96af-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d96af-105">DESCRIPTION</span></span>
<span data-ttu-id="d96af-106">**Register-AzProviderFeature** cmdlet registrerar en Azure Provider-funktion på ditt konto.</span><span class="sxs-lookup"><span data-stu-id="d96af-106">The **Register-AzProviderFeature** cmdlet registers an Azure provider feature in your account.</span></span>

## <span data-ttu-id="d96af-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d96af-107">EXAMPLES</span></span>

### <span data-ttu-id="d96af-108">Exempel 1: registrera en funktion</span><span class="sxs-lookup"><span data-stu-id="d96af-108">Example 1: Register a feature</span></span>
```
PS C:\>Register-AzProviderFeature -FeatureName AllowApplicationSecurityGroups -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="d96af-109">Då läggs AllowApplicationSecurityGroups-funktionen till i ditt konto.</span><span class="sxs-lookup"><span data-stu-id="d96af-109">This adds the AllowApplicationSecurityGroups feature for Microsoft.Network to your account.</span></span>

## <span data-ttu-id="d96af-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d96af-110">PARAMETERS</span></span>

### <span data-ttu-id="d96af-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d96af-111">-DefaultProfile</span></span>
<span data-ttu-id="d96af-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="d96af-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d96af-113">-FeatureName</span><span class="sxs-lookup"><span data-stu-id="d96af-113">-FeatureName</span></span>
<span data-ttu-id="d96af-114">Anger namnet på den funktion som den här cmdleten registrerar.</span><span class="sxs-lookup"><span data-stu-id="d96af-114">Specifies the name of the feature that this cmdlet registers.</span></span>

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

### <span data-ttu-id="d96af-115">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="d96af-115">-ProviderNamespace</span></span>
<span data-ttu-id="d96af-116">Anger ett namn område som denna cmdlet registrerar en leverantörs funktion för.</span><span class="sxs-lookup"><span data-stu-id="d96af-116">Specifies a namespace for which this cmdlet registers a provider feature.</span></span>

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

### <span data-ttu-id="d96af-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d96af-117">-Confirm</span></span>
<span data-ttu-id="d96af-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d96af-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d96af-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d96af-119">-WhatIf</span></span>
<span data-ttu-id="d96af-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d96af-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d96af-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d96af-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d96af-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d96af-122">CommonParameters</span></span>
<span data-ttu-id="d96af-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d96af-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d96af-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d96af-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d96af-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d96af-125">INPUTS</span></span>

### <span data-ttu-id="d96af-126">System. String</span><span class="sxs-lookup"><span data-stu-id="d96af-126">System.String</span></span>

## <span data-ttu-id="d96af-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d96af-127">OUTPUTS</span></span>

### <span data-ttu-id="d96af-128">Microsoft. Azure. kommandon. ResourceManager. cmdlets. SdkModels. PSProviderFeature</span><span class="sxs-lookup"><span data-stu-id="d96af-128">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature</span></span>

## <span data-ttu-id="d96af-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d96af-129">NOTES</span></span>

## <span data-ttu-id="d96af-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d96af-130">RELATED LINKS</span></span>

[<span data-ttu-id="d96af-131">Get-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="d96af-131">Get-AzProviderFeature</span></span>](./Get-AzProviderFeature.md)

