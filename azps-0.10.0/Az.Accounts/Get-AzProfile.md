---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Get-AzProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Get-AzProfile.md
ms.openlocfilehash: d541c943c8dc9779cdf340440078ca2fd2fb36e1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93921986"
---
# <span data-ttu-id="8ee71-101">Get-AzProfile</span><span class="sxs-lookup"><span data-stu-id="8ee71-101">Get-AzProfile</span></span>

## <span data-ttu-id="8ee71-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8ee71-102">SYNOPSIS</span></span>
<span data-ttu-id="8ee71-103">Hämta tjänst profiler som stöds av installerade moduler.</span><span class="sxs-lookup"><span data-stu-id="8ee71-103">Get the service profiles supported by installed modules.</span></span>

## <span data-ttu-id="8ee71-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8ee71-104">SYNTAX</span></span>

```
Get-AzProfile [-ModuleName <String[]>] [-ListAvailable] [<CommonParameters>]
```

## <span data-ttu-id="8ee71-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8ee71-105">DESCRIPTION</span></span>
<span data-ttu-id="8ee71-106">Hämta tjänst profiler som stöds av installerade moduler.</span><span class="sxs-lookup"><span data-stu-id="8ee71-106">Get the service profiles supported by installed modules.</span></span>

## <span data-ttu-id="8ee71-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8ee71-107">EXAMPLES</span></span>

### <span data-ttu-id="8ee71-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="8ee71-108">Example 1</span></span>
```powershell
PS C:\> Get-AzProfile -ModuleName Az.KeyVault

Name              Description
----              -----------
latest-2019-04-30 A snapshot of the service API versions in the Azure Global Cloud. This profile was defined in April 2019.
hybrid-2019-03-01 A snapshot of the Service API versions in AzureStack, Azure Sovereign clouds, and the Azure Global Cloud. This profile was defined                    in March 2019.
```

<span data-ttu-id="8ee71-109">Hämta tjänst profilen som stöds av modulen för valv</span><span class="sxs-lookup"><span data-stu-id="8ee71-109">Get the service profile supported by the KeyVault module</span></span>

## <span data-ttu-id="8ee71-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8ee71-110">PARAMETERS</span></span>

### <span data-ttu-id="8ee71-111">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="8ee71-111">-ListAvailable</span></span>
<span data-ttu-id="8ee71-112">Visa alla tjänst profiler som stöds av installerade moduler</span><span class="sxs-lookup"><span data-stu-id="8ee71-112">List all service profiles supported by installed modules</span></span>

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

### <span data-ttu-id="8ee71-113">-ModuleName</span><span class="sxs-lookup"><span data-stu-id="8ee71-113">-ModuleName</span></span>
<span data-ttu-id="8ee71-114">Namnet på den modul som ska kontrol leras</span><span class="sxs-lookup"><span data-stu-id="8ee71-114">The name of the module to check</span></span>

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

### <span data-ttu-id="8ee71-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ee71-115">CommonParameters</span></span>
<span data-ttu-id="8ee71-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ee71-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ee71-117">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8ee71-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ee71-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8ee71-118">INPUTS</span></span>

### <span data-ttu-id="8ee71-119">Ingen</span><span class="sxs-lookup"><span data-stu-id="8ee71-119">None</span></span>

## <span data-ttu-id="8ee71-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8ee71-120">OUTPUTS</span></span>

### <span data-ttu-id="8ee71-121">Microsoft. Azure. commands. Profile. CommonModule. PSAzureServiceProfile</span><span class="sxs-lookup"><span data-stu-id="8ee71-121">Microsoft.Azure.Commands.Profile.CommonModule.PSAzureServiceProfile</span></span>

## <span data-ttu-id="8ee71-122">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8ee71-122">NOTES</span></span>

## <span data-ttu-id="8ee71-123">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8ee71-123">RELATED LINKS</span></span>
