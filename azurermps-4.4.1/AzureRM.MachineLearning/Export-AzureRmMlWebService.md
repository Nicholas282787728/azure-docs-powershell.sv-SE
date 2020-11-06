---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Export-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Export-AzureRmMlWebService.md
ms.openlocfilehash: f8923c6f98dad44a56c35cadc4b3e1daedeb1227
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580592"
---
# <span data-ttu-id="4cc7f-101">Export-AzureRmMlWebService</span><span class="sxs-lookup"><span data-stu-id="4cc7f-101">Export-AzureRmMlWebService</span></span>

## <span data-ttu-id="4cc7f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4cc7f-102">SYNOPSIS</span></span>
<span data-ttu-id="4cc7f-103">Exporterar webb tjänst definitions objekt som en JSON-formaterad sträng.</span><span class="sxs-lookup"><span data-stu-id="4cc7f-103">Exports the web service definition object as a JSON formatted string.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4cc7f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4cc7f-104">SYNTAX</span></span>

### <span data-ttu-id="4cc7f-105">Exportera till fil.</span><span class="sxs-lookup"><span data-stu-id="4cc7f-105">Export to file.</span></span>
```
Export-AzureRmMlWebService -WebService <WebService> -OutputFile <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4cc7f-106">Exportera till JSON-sträng.</span><span class="sxs-lookup"><span data-stu-id="4cc7f-106">Export to JSON string.</span></span>
```
Export-AzureRmMlWebService -WebService <WebService> [-ToJsonString] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4cc7f-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4cc7f-107">DESCRIPTION</span></span>
<span data-ttu-id="4cc7f-108">Exporterar definitionsfiler för den angivna webb serving som en JSON-formaterad sträng.</span><span class="sxs-lookup"><span data-stu-id="4cc7f-108">Exports the definition object for the specified web servive as a JSON formatted string.</span></span>
<span data-ttu-id="4cc7f-109">Du kan returnera strängen direkt eller spara den i en fil.</span><span class="sxs-lookup"><span data-stu-id="4cc7f-109">You can return the string immediately or save it to a file.</span></span>

## <span data-ttu-id="4cc7f-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4cc7f-110">EXAMPLES</span></span>

### <span data-ttu-id="4cc7f-111">--------------------------Exempel 1: exportera som sträng--------------------------</span><span class="sxs-lookup"><span data-stu-id="4cc7f-111">--------------------------  Example 1: Export as string  --------------------------</span></span>
<span data-ttu-id="4cc7f-112">@ {paragraf = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="4cc7f-112">@{paragraph=PS C:\\\>}</span></span>





```
Export-AzureRmMlWebService -WebService $svc -ToJsonString
```

### <span data-ttu-id="4cc7f-113">--------------------------Exempel 2: exportera till fil--------------------------</span><span class="sxs-lookup"><span data-stu-id="4cc7f-113">--------------------------  Example 2: Export to file  --------------------------</span></span>
<span data-ttu-id="4cc7f-114">@ {paragraf = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="4cc7f-114">@{paragraph=PS C:\\\>}</span></span>





```
Export-AzureRmMlWebService -WebService $svc -OutputFile "C:\mlservice.json"
```

## <span data-ttu-id="4cc7f-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4cc7f-115">PARAMETERS</span></span>

### <span data-ttu-id="4cc7f-116">-Force</span><span class="sxs-lookup"><span data-stu-id="4cc7f-116">-Force</span></span>
<span data-ttu-id="4cc7f-117">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="4cc7f-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="4cc7f-118">-Utdatafil</span><span class="sxs-lookup"><span data-stu-id="4cc7f-118">-OutputFile</span></span>
<span data-ttu-id="4cc7f-119">Sökvägen till den exporterade definitionen.</span><span class="sxs-lookup"><span data-stu-id="4cc7f-119">The file path for exported definition.</span></span>

```yaml
Type: System.String
Parameter Sets: Export to file.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cc7f-120">-ToJsonString</span><span class="sxs-lookup"><span data-stu-id="4cc7f-120">-ToJsonString</span></span>
<span data-ttu-id="4cc7f-121">Anger att definitionen exporteras som en JSON-sträng.</span><span class="sxs-lookup"><span data-stu-id="4cc7f-121">Specifies that the definition will be exported as a JSON string.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Export to JSON string.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cc7f-122">-Webservice</span><span class="sxs-lookup"><span data-stu-id="4cc7f-122">-WebService</span></span>
<span data-ttu-id="4cc7f-123">Webb tjänst definitions objekt som ska exporteras.</span><span class="sxs-lookup"><span data-stu-id="4cc7f-123">The web service definition object to be exported.</span></span>

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

### <span data-ttu-id="4cc7f-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4cc7f-124">-Confirm</span></span>
<span data-ttu-id="4cc7f-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4cc7f-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4cc7f-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4cc7f-126">-WhatIf</span></span>
<span data-ttu-id="4cc7f-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4cc7f-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4cc7f-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4cc7f-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4cc7f-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cc7f-129">-DefaultProfile</span></span>
<span data-ttu-id="4cc7f-130">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4cc7f-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cc7f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cc7f-131">CommonParameters</span></span>
<span data-ttu-id="4cc7f-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4cc7f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cc7f-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4cc7f-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cc7f-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4cc7f-134">INPUTS</span></span>

### <span data-ttu-id="4cc7f-135">Webb tjänst</span><span class="sxs-lookup"><span data-stu-id="4cc7f-135">WebService</span></span>
<span data-ttu-id="4cc7f-136">Parametern "WebService" accepterar värdet för typen "WebService" från pipeline</span><span class="sxs-lookup"><span data-stu-id="4cc7f-136">Parameter 'WebService' accepts value of type 'WebService' from the pipeline</span></span>

## <span data-ttu-id="4cc7f-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4cc7f-137">OUTPUTS</span></span>

### <span data-ttu-id="4cc7f-138">Ingen</span><span class="sxs-lookup"><span data-stu-id="4cc7f-138">None</span></span>

## <span data-ttu-id="4cc7f-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4cc7f-139">NOTES</span></span>
<span data-ttu-id="4cc7f-140">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, maskin, maskin inlärning, azureml</span><span class="sxs-lookup"><span data-stu-id="4cc7f-140">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="4cc7f-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4cc7f-141">RELATED LINKS</span></span>

