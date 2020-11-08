---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/select-azprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Select-AzProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Select-AzProfile.md
ms.openlocfilehash: 1ca2244d4ed1a47535a228ed772d9d9a6ecb6acb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088947"
---
# <span data-ttu-id="69bf8-101">Select-AzProfile</span><span class="sxs-lookup"><span data-stu-id="69bf8-101">Select-AzProfile</span></span>

## <span data-ttu-id="69bf8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="69bf8-102">SYNOPSIS</span></span>
<span data-ttu-id="69bf8-103">För moduler som stöder flera tjänst profiler-Ladda cmdletarna som motsvarar den angivna tjänst profilen.</span><span class="sxs-lookup"><span data-stu-id="69bf8-103">For modules that support multiple service profiles - load the cmdlets corresponding with the given service profile.</span></span>

## <span data-ttu-id="69bf8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="69bf8-104">SYNTAX</span></span>

```
Select-AzProfile -Name <String> [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69bf8-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="69bf8-105">DESCRIPTION</span></span>
<span data-ttu-id="69bf8-106">För moduler som stöder flera tjänst profiler-Ladda cmdletarna som motsvarar den angivna tjänst profilen.</span><span class="sxs-lookup"><span data-stu-id="69bf8-106">For modules that support multiple service profiles - load the cmdlets corresponding with the given service profile.</span></span>

## <span data-ttu-id="69bf8-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="69bf8-107">EXAMPLES</span></span>

### <span data-ttu-id="69bf8-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="69bf8-108">Example 1</span></span>
```powershell
PS C:\> Select-AzProfile hybrid-2019-03
```

<span data-ttu-id="69bf8-109">Ladda cmdletar för AzureStack-profilen från mars 2019</span><span class="sxs-lookup"><span data-stu-id="69bf8-109">Load cmdlets for the AzureStack profile from March 2019</span></span>

## <span data-ttu-id="69bf8-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="69bf8-110">PARAMETERS</span></span>

### <span data-ttu-id="69bf8-111">-Namn</span><span class="sxs-lookup"><span data-stu-id="69bf8-111">-Name</span></span>
<span data-ttu-id="69bf8-112">Namnet på profilen som ska väljas</span><span class="sxs-lookup"><span data-stu-id="69bf8-112">The name of the profile to select</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ProfileName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69bf8-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="69bf8-113">-PassThru</span></span>
<span data-ttu-id="69bf8-114">När det här alternativet är aktiverat tvingar cmdleten att returnera ett värde när den lyckas</span><span class="sxs-lookup"><span data-stu-id="69bf8-114">When present, forces the cmdlet to return a value on successful execution</span></span>

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

### <span data-ttu-id="69bf8-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="69bf8-115">-Confirm</span></span>
<span data-ttu-id="69bf8-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="69bf8-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69bf8-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69bf8-117">-WhatIf</span></span>
<span data-ttu-id="69bf8-118">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="69bf8-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69bf8-119">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="69bf8-119">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69bf8-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69bf8-120">CommonParameters</span></span>
<span data-ttu-id="69bf8-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69bf8-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69bf8-122">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69bf8-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69bf8-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="69bf8-123">INPUTS</span></span>

### <span data-ttu-id="69bf8-124">Ingen</span><span class="sxs-lookup"><span data-stu-id="69bf8-124">None</span></span>

## <span data-ttu-id="69bf8-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="69bf8-125">OUTPUTS</span></span>

### <span data-ttu-id="69bf8-126">System. Object</span><span class="sxs-lookup"><span data-stu-id="69bf8-126">System.Object</span></span>
## <span data-ttu-id="69bf8-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="69bf8-127">NOTES</span></span>

## <span data-ttu-id="69bf8-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="69bf8-128">RELATED LINKS</span></span>