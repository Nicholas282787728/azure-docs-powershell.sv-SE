---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 9960a34d19c4016461ddfc53a37f83d3e73e7526
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757302"
---
# <span data-ttu-id="8c97f-101">New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential</span><span class="sxs-lookup"><span data-stu-id="8c97f-101">New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential</span></span>

## <span data-ttu-id="8c97f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8c97f-102">SYNOPSIS</span></span>
<span data-ttu-id="8c97f-103">Kryptera Credential i den länkade tjänsten med den angivna integrerings körningen.</span><span class="sxs-lookup"><span data-stu-id="8c97f-103">Encrypt credential in linked service with specified integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8c97f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8c97f-104">SYNTAX</span></span>

### <span data-ttu-id="8c97f-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="8c97f-105">ByFactoryName (Default)</span></span>
```
New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential [-IntegrationRuntimeName] <String>
 [-DefinitionFile] <String> [-Force] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="8c97f-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="8c97f-106">ByFactoryObject</span></span>
```
New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential [-IntegrationRuntimeName] <String>
 [-DefinitionFile] <String> [-Force] [-DataFactory] <PSDataFactory>
 [-WhatIf] [-Confirm]
```

## <span data-ttu-id="8c97f-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8c97f-107">DESCRIPTION</span></span>
<span data-ttu-id="8c97f-108">New-AzureRmDataFactoryV2LinkedServiceEncryptCredential cmdlet krypterar autentiseringsuppgiften i den länkade tjänsten med den angivna integrerings körnings miljön.</span><span class="sxs-lookup"><span data-stu-id="8c97f-108">The New-AzureRmDataFactoryV2LinkedServiceEncryptCredential cmdlet encrypt credential in linked service with specified integration runtime.</span></span>

## <span data-ttu-id="8c97f-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8c97f-109">EXAMPLES</span></span>

### <span data-ttu-id="8c97f-110">Exempel 1: kryptera creadentials i en länkad tjänst</span><span class="sxs-lookup"><span data-stu-id="8c97f-110">Example 1: Encrypt creadentials in a linked service</span></span>
```
PS C:\> New-AzureRmDataFactoryV2LinkedServiceEncryptCredential -ResourceGroupName resourceGroup -DataFactoryName myDataFactory -IntegrationRuntimeName myIR -File D:\sql.json
```

<span data-ttu-id="8c97f-111">Det här kommandot krypterar autentiseringsuppgifter i fil D:\sql.jsmed integrerings programmet med namnet myIR.</span><span class="sxs-lookup"><span data-stu-id="8c97f-111">This command encrypts credential in file D:\sql.json with the integration runtime named myIR.</span></span>

## <span data-ttu-id="8c97f-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8c97f-112">PARAMETERS</span></span>

### <span data-ttu-id="8c97f-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="8c97f-113">-DataFactory</span></span>
<span data-ttu-id="8c97f-114">Data fabriks objekt.</span><span class="sxs-lookup"><span data-stu-id="8c97f-114">The data factory object.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8c97f-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="8c97f-115">-DataFactoryName</span></span>
<span data-ttu-id="8c97f-116">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="8c97f-116">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c97f-117">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="8c97f-117">-DefinitionFile</span></span>
<span data-ttu-id="8c97f-118">Sökvägen till JSON-filen.</span><span class="sxs-lookup"><span data-stu-id="8c97f-118">The JSON file path.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c97f-119">-Force</span><span class="sxs-lookup"><span data-stu-id="8c97f-119">-Force</span></span>
<span data-ttu-id="8c97f-120">Kör cmdleten utan att behöva bekräfta.</span><span class="sxs-lookup"><span data-stu-id="8c97f-120">Runs the cmdlet without prompting for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c97f-121">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="8c97f-121">-IntegrationRuntimeName</span></span>
<span data-ttu-id="8c97f-122">Integrerings körens namn.</span><span class="sxs-lookup"><span data-stu-id="8c97f-122">The integration runtime name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c97f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c97f-123">-ResourceGroupName</span></span>
<span data-ttu-id="8c97f-124">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="8c97f-124">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c97f-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8c97f-125">-Confirm</span></span>
<span data-ttu-id="8c97f-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8c97f-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c97f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c97f-127">-WhatIf</span></span>
<span data-ttu-id="8c97f-128">Visar vad som händer om cmdleten körs men inte kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8c97f-128">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="8c97f-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8c97f-129">INPUTS</span></span>

### <span data-ttu-id="8c97f-130">System. String</span><span class="sxs-lookup"><span data-stu-id="8c97f-130">System.String</span></span>
<span data-ttu-id="8c97f-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="8c97f-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>


## <span data-ttu-id="8c97f-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8c97f-132">OUTPUTS</span></span>

### <span data-ttu-id="8c97f-133">System. String</span><span class="sxs-lookup"><span data-stu-id="8c97f-133">System.String</span></span>


## <span data-ttu-id="8c97f-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8c97f-134">NOTES</span></span>

## <span data-ttu-id="8c97f-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8c97f-135">RELATED LINKS</span></span>

