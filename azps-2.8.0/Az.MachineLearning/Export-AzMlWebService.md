---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/export-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Export-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Export-AzMlWebService.md
ms.openlocfilehash: 4514c23f4a8c638c5a6ca48752f6ff9ea8343a07
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93743716"
---
# <span data-ttu-id="503d1-101">Export-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="503d1-101">Export-AzMlWebService</span></span>

## <span data-ttu-id="503d1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="503d1-102">SYNOPSIS</span></span>
<span data-ttu-id="503d1-103">Exporterar webb tjänst definitions objekt som en JSON-formaterad sträng.</span><span class="sxs-lookup"><span data-stu-id="503d1-103">Exports the web service definition object as a JSON formatted string.</span></span>

## <span data-ttu-id="503d1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="503d1-104">SYNTAX</span></span>

### <span data-ttu-id="503d1-105">ExportToFile</span><span class="sxs-lookup"><span data-stu-id="503d1-105">ExportToFile</span></span>
```
Export-AzMlWebService -WebService <WebService> -OutputFile <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="503d1-106">ExportToJSON</span><span class="sxs-lookup"><span data-stu-id="503d1-106">ExportToJSON</span></span>
```
Export-AzMlWebService -WebService <WebService> [-ToJsonString] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="503d1-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="503d1-107">DESCRIPTION</span></span>
<span data-ttu-id="503d1-108">Exporterar definitionsfiler för den angivna webb tjänsten som en JSON-formaterad sträng.</span><span class="sxs-lookup"><span data-stu-id="503d1-108">Exports the definition object for the specified web service as a JSON formatted string.</span></span>
<span data-ttu-id="503d1-109">Du kan returnera strängen direkt eller spara den i en fil.</span><span class="sxs-lookup"><span data-stu-id="503d1-109">You can return the string immediately or save it to a file.</span></span>

## <span data-ttu-id="503d1-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="503d1-110">EXAMPLES</span></span>

### <span data-ttu-id="503d1-111">Exempel 1: exportera som sträng</span><span class="sxs-lookup"><span data-stu-id="503d1-111">Example 1: Export as string</span></span>
```
Export-AzMlWebService -WebService $svc -ToJsonString
```

### <span data-ttu-id="503d1-112">Exempel 2: exportera till filen</span><span class="sxs-lookup"><span data-stu-id="503d1-112">Example 2: Export to file</span></span>
```
Export-AzMlWebService -WebService $svc -OutputFile "C:\mlservice.json"
```

## <span data-ttu-id="503d1-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="503d1-113">PARAMETERS</span></span>

### <span data-ttu-id="503d1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="503d1-114">-DefaultProfile</span></span>
<span data-ttu-id="503d1-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="503d1-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="503d1-116">-Force</span><span class="sxs-lookup"><span data-stu-id="503d1-116">-Force</span></span>
<span data-ttu-id="503d1-117">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="503d1-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="503d1-118">-Utdatafil</span><span class="sxs-lookup"><span data-stu-id="503d1-118">-OutputFile</span></span>
<span data-ttu-id="503d1-119">Sökvägen till den exporterade definitionen.</span><span class="sxs-lookup"><span data-stu-id="503d1-119">The file path for exported definition.</span></span>

```yaml
Type: System.String
Parameter Sets: ExportToFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="503d1-120">-ToJsonString</span><span class="sxs-lookup"><span data-stu-id="503d1-120">-ToJsonString</span></span>
<span data-ttu-id="503d1-121">Anger att definitionen exporteras som en JSON-sträng.</span><span class="sxs-lookup"><span data-stu-id="503d1-121">Specifies that the definition will be exported as a JSON string.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ExportToJSON
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="503d1-122">-Webservice</span><span class="sxs-lookup"><span data-stu-id="503d1-122">-WebService</span></span>
<span data-ttu-id="503d1-123">Webb tjänst definitions objekt som ska exporteras.</span><span class="sxs-lookup"><span data-stu-id="503d1-123">The web service definition object to be exported.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="503d1-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="503d1-124">-Confirm</span></span>
<span data-ttu-id="503d1-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="503d1-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="503d1-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="503d1-126">-WhatIf</span></span>
<span data-ttu-id="503d1-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="503d1-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="503d1-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="503d1-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="503d1-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="503d1-129">CommonParameters</span></span>
<span data-ttu-id="503d1-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="503d1-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="503d1-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="503d1-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="503d1-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="503d1-132">INPUTS</span></span>

### <span data-ttu-id="503d1-133">Microsoft. Azure. Management. MachineLearning. WebServices. Models. WebService</span><span class="sxs-lookup"><span data-stu-id="503d1-133">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="503d1-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="503d1-134">OUTPUTS</span></span>

### <span data-ttu-id="503d1-135">System. String</span><span class="sxs-lookup"><span data-stu-id="503d1-135">System.String</span></span>

## <span data-ttu-id="503d1-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="503d1-136">NOTES</span></span>
<span data-ttu-id="503d1-137">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, maskin, maskin inlärning, azureml</span><span class="sxs-lookup"><span data-stu-id="503d1-137">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="503d1-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="503d1-138">RELATED LINKS</span></span>