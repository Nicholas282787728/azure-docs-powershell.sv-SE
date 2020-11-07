---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzProfile.md
ms.openlocfilehash: 937683c8592bb814b7f6a6262ef095cbd8252c78
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745976"
---
# <span data-ttu-id="b59d4-101">Get-AzProfile</span><span class="sxs-lookup"><span data-stu-id="b59d4-101">Get-AzProfile</span></span>

## <span data-ttu-id="b59d4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b59d4-102">SYNOPSIS</span></span>
<span data-ttu-id="b59d4-103">Hämta tjänst profiler som stöds av installerade moduler.</span><span class="sxs-lookup"><span data-stu-id="b59d4-103">Get the service profiles supported by installed modules.</span></span>

## <span data-ttu-id="b59d4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b59d4-104">SYNTAX</span></span>

```
Get-AzProfile [-ModuleName <String[]>] [-ListAvailable] [<CommonParameters>]
```

## <span data-ttu-id="b59d4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b59d4-105">DESCRIPTION</span></span>
<span data-ttu-id="b59d4-106">Hämta tjänst profiler som stöds av installerade moduler.</span><span class="sxs-lookup"><span data-stu-id="b59d4-106">Get the service profiles supported by installed modules.</span></span>

## <span data-ttu-id="b59d4-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b59d4-107">EXAMPLES</span></span>

### <span data-ttu-id="b59d4-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b59d4-108">Example 1</span></span>
```powershell
PS C:\> Get-AzProfile -ModuleName Az.KeyVault

Name              Description
----              -----------
latest-2019-04-30 A snapshot of the service API versions in the Azure Global Cloud. This profile was defined in April 2019.
hybrid-2019-03-01 A snapshot of the Service API versions in AzureStack, Azure Sovereign clouds, and the Azure Global Cloud. This profile was defined                    in March 2019.
```

<span data-ttu-id="b59d4-109">Hämta tjänst profilen som stöds av modulen för valv</span><span class="sxs-lookup"><span data-stu-id="b59d4-109">Get the service profile supported by the KeyVault module</span></span>

## <span data-ttu-id="b59d4-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b59d4-110">PARAMETERS</span></span>

### <span data-ttu-id="b59d4-111">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="b59d4-111">-ListAvailable</span></span>
<span data-ttu-id="b59d4-112">Visa alla tjänst profiler som stöds av installerade moduler</span><span class="sxs-lookup"><span data-stu-id="b59d4-112">List all service profiles supported by installed modules</span></span>

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

### <span data-ttu-id="b59d4-113">-ModuleName</span><span class="sxs-lookup"><span data-stu-id="b59d4-113">-ModuleName</span></span>
<span data-ttu-id="b59d4-114">Namnet på den modul som ska kontrol leras</span><span class="sxs-lookup"><span data-stu-id="b59d4-114">The name of the module to check</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b59d4-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b59d4-115">CommonParameters</span></span>
<span data-ttu-id="b59d4-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b59d4-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b59d4-117">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b59d4-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b59d4-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b59d4-118">INPUTS</span></span>

### <span data-ttu-id="b59d4-119">Ingen</span><span class="sxs-lookup"><span data-stu-id="b59d4-119">None</span></span>

## <span data-ttu-id="b59d4-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b59d4-120">OUTPUTS</span></span>

### <span data-ttu-id="b59d4-121">Microsoft. Azure. commands. Profile. CommonModule. PSAzureServiceProfile</span><span class="sxs-lookup"><span data-stu-id="b59d4-121">Microsoft.Azure.Commands.Profile.CommonModule.PSAzureServiceProfile</span></span>

## <span data-ttu-id="b59d4-122">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b59d4-122">NOTES</span></span>

## <span data-ttu-id="b59d4-123">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b59d4-123">RELATED LINKS</span></span>
