---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmruncommanddocument
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMRunCommandDocument.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMRunCommandDocument.md
ms.openlocfilehash: 5aeb8d7ba44f07519ff3cdfdc5e775687bd98260
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98526939"
---
# <span data-ttu-id="e8cf8-101">Get-AzVMRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="e8cf8-101">Get-AzVMRunCommandDocument</span></span>

## <span data-ttu-id="e8cf8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e8cf8-102">SYNOPSIS</span></span>
<span data-ttu-id="e8cf8-103">Hämta ett kommando dokument för kör.</span><span class="sxs-lookup"><span data-stu-id="e8cf8-103">Get a run command document.</span></span>

## <span data-ttu-id="e8cf8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e8cf8-104">SYNTAX</span></span>

```
Get-AzVMRunCommandDocument [-Location] <String> [[-CommandId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8cf8-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e8cf8-105">DESCRIPTION</span></span>
<span data-ttu-id="e8cf8-106">Hämta ett kommando dokument för kör.</span><span class="sxs-lookup"><span data-stu-id="e8cf8-106">Get a run command document.</span></span>

## <span data-ttu-id="e8cf8-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e8cf8-107">EXAMPLES</span></span>

### <span data-ttu-id="e8cf8-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e8cf8-108">Example 1</span></span>
```
PS C:\> Get-AzVMRunCommandDocument -Location 'westus' -CommandId 'RunPowerShellScript'
```

<span data-ttu-id="e8cf8-109">Hämtar ett specifikt kommando dokument för "RunPowerShellScript" i "västkusten".</span><span class="sxs-lookup"><span data-stu-id="e8cf8-109">Gets a specific run command document for 'RunPowerShellScript' in 'westus'.</span></span>

### <span data-ttu-id="e8cf8-110">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="e8cf8-110">Example 2</span></span>
```
PS C:\> Get-AzVMRunCommandDocument -Location 'westus'
```

<span data-ttu-id="e8cf8-111">Visar alla tillgängliga kör-kommandon i "västkusten".</span><span class="sxs-lookup"><span data-stu-id="e8cf8-111">Lists all available run commands in 'westus'.</span></span>

## <span data-ttu-id="e8cf8-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e8cf8-112">PARAMETERS</span></span>

### <span data-ttu-id="e8cf8-113">-CommandId</span><span class="sxs-lookup"><span data-stu-id="e8cf8-113">-CommandId</span></span>
<span data-ttu-id="e8cf8-114">Kommando-ID.</span><span class="sxs-lookup"><span data-stu-id="e8cf8-114">The command ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8cf8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8cf8-115">-DefaultProfile</span></span>
<span data-ttu-id="e8cf8-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e8cf8-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8cf8-117">-Plats</span><span class="sxs-lookup"><span data-stu-id="e8cf8-117">-Location</span></span>
<span data-ttu-id="e8cf8-118">Den plats där kommandona körs.</span><span class="sxs-lookup"><span data-stu-id="e8cf8-118">The location upon which run commands are queried.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8cf8-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8cf8-119">CommonParameters</span></span>
<span data-ttu-id="e8cf8-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8cf8-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8cf8-121">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e8cf8-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8cf8-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e8cf8-122">INPUTS</span></span>

### <span data-ttu-id="e8cf8-123">System. String</span><span class="sxs-lookup"><span data-stu-id="e8cf8-123">System.String</span></span>

## <span data-ttu-id="e8cf8-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e8cf8-124">OUTPUTS</span></span>

### <span data-ttu-id="e8cf8-125">Microsoft. Azure. commands. Compute. Automation. Models. PSRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="e8cf8-125">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandDocument</span></span>

## <span data-ttu-id="e8cf8-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e8cf8-126">NOTES</span></span>

## <span data-ttu-id="e8cf8-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e8cf8-127">RELATED LINKS</span></span>
