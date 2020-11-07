---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmruncommanddocument
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMRunCommandDocument.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMRunCommandDocument.md
ms.openlocfilehash: 45d051e5fc2fe750f58dc6400a037960b7eb9c7c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93925150"
---
# <span data-ttu-id="2a17d-101">Get-AzVMRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="2a17d-101">Get-AzVMRunCommandDocument</span></span>

## <span data-ttu-id="2a17d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2a17d-102">SYNOPSIS</span></span>
<span data-ttu-id="2a17d-103">Kommandot Hämta kommando.</span><span class="sxs-lookup"><span data-stu-id="2a17d-103">Get run command document.</span></span>

## <span data-ttu-id="2a17d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2a17d-104">SYNTAX</span></span>

```
Get-AzVMRunCommandDocument [-Location] <String> [[-CommandId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2a17d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2a17d-105">DESCRIPTION</span></span>
<span data-ttu-id="2a17d-106">Kommandot Hämta kommando.</span><span class="sxs-lookup"><span data-stu-id="2a17d-106">Get run command document.</span></span>

## <span data-ttu-id="2a17d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2a17d-107">EXAMPLES</span></span>

### <span data-ttu-id="2a17d-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="2a17d-108">Example 1</span></span>
```
PS C:\> Get-AzVMRunCommandDocument -Location 'westus' -CommandId 'RunPowerShellScript'
```

<span data-ttu-id="2a17d-109">Hämtar ett specifikt kommando dokument för "RunPowerShellScript" i "västkusten".</span><span class="sxs-lookup"><span data-stu-id="2a17d-109">Gets a specific run command document for 'RunPowerShellScript' in 'westus'.</span></span>


<span data-ttu-id="2a17d-110">Get-AzVMRunCommandDocument plats $loc</span><span class="sxs-lookup"><span data-stu-id="2a17d-110">Get-AzVMRunCommandDocument -Location $loc</span></span>

### <span data-ttu-id="2a17d-111">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="2a17d-111">Example 2</span></span>
```
PS C:\> Get-AzVMRunCommandDocument -Location 'westus'
```

<span data-ttu-id="2a17d-112">Visar alla tillgängliga kör-kommandon i "västkusten".</span><span class="sxs-lookup"><span data-stu-id="2a17d-112">Lists all available run commands in 'westus'.</span></span>

## <span data-ttu-id="2a17d-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2a17d-113">PARAMETERS</span></span>

### <span data-ttu-id="2a17d-114">-CommandId</span><span class="sxs-lookup"><span data-stu-id="2a17d-114">-CommandId</span></span>
<span data-ttu-id="2a17d-115">Kommando-ID.</span><span class="sxs-lookup"><span data-stu-id="2a17d-115">The command id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a17d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a17d-116">-DefaultProfile</span></span>
<span data-ttu-id="2a17d-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2a17d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a17d-118">-Plats</span><span class="sxs-lookup"><span data-stu-id="2a17d-118">-Location</span></span>
<span data-ttu-id="2a17d-119">Den plats där kommandona körs.</span><span class="sxs-lookup"><span data-stu-id="2a17d-119">The location upon which run commands is queried.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a17d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a17d-120">CommonParameters</span></span>
<span data-ttu-id="2a17d-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a17d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a17d-122">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a17d-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a17d-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2a17d-123">INPUTS</span></span>

### <span data-ttu-id="2a17d-124">System. String</span><span class="sxs-lookup"><span data-stu-id="2a17d-124">System.String</span></span>

## <span data-ttu-id="2a17d-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2a17d-125">OUTPUTS</span></span>

### <span data-ttu-id="2a17d-126">Microsoft. Azure. commands. Compute. Automation. Models. PSRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="2a17d-126">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandDocument</span></span>

## <span data-ttu-id="2a17d-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2a17d-127">NOTES</span></span>

## <span data-ttu-id="2a17d-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2a17d-128">RELATED LINKS</span></span>

