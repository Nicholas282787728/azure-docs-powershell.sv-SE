---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmruncommanddocument
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMRunCommandDocument.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMRunCommandDocument.md
ms.openlocfilehash: 3b66cdc6574397de7d43dfef0677a5ddac772a31
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745147"
---
# <span data-ttu-id="8c4df-101">Get-AzVMRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="8c4df-101">Get-AzVMRunCommandDocument</span></span>

## <span data-ttu-id="8c4df-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8c4df-102">SYNOPSIS</span></span>
<span data-ttu-id="8c4df-103">Hämta ett kommando dokument för kör.</span><span class="sxs-lookup"><span data-stu-id="8c4df-103">Get a run command document.</span></span>

## <span data-ttu-id="8c4df-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8c4df-104">SYNTAX</span></span>

```
Get-AzVMRunCommandDocument [-Location] <String> [[-CommandId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8c4df-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8c4df-105">DESCRIPTION</span></span>
<span data-ttu-id="8c4df-106">Hämta ett kommando dokument för kör.</span><span class="sxs-lookup"><span data-stu-id="8c4df-106">Get a run command document.</span></span>

## <span data-ttu-id="8c4df-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8c4df-107">EXAMPLES</span></span>

### <span data-ttu-id="8c4df-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="8c4df-108">Example 1</span></span>
```
PS C:\> Get-AzVMRunCommandDocument -Location 'westus' -CommandId 'RunPowerShellScript'
```

<span data-ttu-id="8c4df-109">Hämtar ett specifikt kommando dokument för "RunPowerShellScript" i "västkusten".</span><span class="sxs-lookup"><span data-stu-id="8c4df-109">Gets a specific run command document for 'RunPowerShellScript' in 'westus'.</span></span>

### <span data-ttu-id="8c4df-110">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="8c4df-110">Example 2</span></span>
```
PS C:\> Get-AzVMRunCommandDocument -Location 'westus'
```

<span data-ttu-id="8c4df-111">Visar alla tillgängliga kör-kommandon i "västkusten".</span><span class="sxs-lookup"><span data-stu-id="8c4df-111">Lists all available run commands in 'westus'.</span></span>

## <span data-ttu-id="8c4df-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8c4df-112">PARAMETERS</span></span>

### <span data-ttu-id="8c4df-113">-CommandId</span><span class="sxs-lookup"><span data-stu-id="8c4df-113">-CommandId</span></span>
<span data-ttu-id="8c4df-114">Kommando-ID.</span><span class="sxs-lookup"><span data-stu-id="8c4df-114">The command ID.</span></span>

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

### <span data-ttu-id="8c4df-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c4df-115">-DefaultProfile</span></span>
<span data-ttu-id="8c4df-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8c4df-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c4df-117">-Plats</span><span class="sxs-lookup"><span data-stu-id="8c4df-117">-Location</span></span>
<span data-ttu-id="8c4df-118">Den plats där kommandona körs.</span><span class="sxs-lookup"><span data-stu-id="8c4df-118">The location upon which run commands are queried.</span></span>

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

### <span data-ttu-id="8c4df-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c4df-119">CommonParameters</span></span>
<span data-ttu-id="8c4df-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c4df-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c4df-121">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8c4df-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c4df-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8c4df-122">INPUTS</span></span>

### <span data-ttu-id="8c4df-123">System. String</span><span class="sxs-lookup"><span data-stu-id="8c4df-123">System.String</span></span>

## <span data-ttu-id="8c4df-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8c4df-124">OUTPUTS</span></span>

### <span data-ttu-id="8c4df-125">Microsoft. Azure. commands. Compute. Automation. Models. PSRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="8c4df-125">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandDocument</span></span>

## <span data-ttu-id="8c4df-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8c4df-126">NOTES</span></span>

## <span data-ttu-id="8c4df-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8c4df-127">RELATED LINKS</span></span>
