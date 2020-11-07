---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/new-azurermdatafactoryv2linkedserviceencryptedcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential.md
ms.openlocfilehash: 47121a8a06e2b4aa4e48218d1be4694743c00de0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573470"
---
# <span data-ttu-id="a901a-101">New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential</span><span class="sxs-lookup"><span data-stu-id="a901a-101">New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential</span></span>

## <span data-ttu-id="a901a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a901a-102">SYNOPSIS</span></span>
<span data-ttu-id="a901a-103">Kryptera Credential i den länkade tjänsten med den angivna integrerings körningen.</span><span class="sxs-lookup"><span data-stu-id="a901a-103">Encrypt credential in linked service with specified integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a901a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a901a-104">SYNTAX</span></span>

### <span data-ttu-id="a901a-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="a901a-105">ByFactoryName (Default)</span></span>
```
New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential [-IntegrationRuntimeName] <String>
 [-DefinitionFile] <String> [-Force] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a901a-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="a901a-106">ByFactoryObject</span></span>
```
New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential [-IntegrationRuntimeName] <String>
 [-DefinitionFile] <String> [-Force] [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a901a-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a901a-107">DESCRIPTION</span></span>
<span data-ttu-id="a901a-108">New-AzureRmDataFactoryV2LinkedServiceEncryptCredential cmdlet krypterar autentiseringsuppgiften i den länkade tjänsten med den angivna integrerings körnings miljön.</span><span class="sxs-lookup"><span data-stu-id="a901a-108">The New-AzureRmDataFactoryV2LinkedServiceEncryptCredential cmdlet encrypt credential in linked service with specified integration runtime.</span></span>

## <span data-ttu-id="a901a-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a901a-109">EXAMPLES</span></span>

### <span data-ttu-id="a901a-110">Exempel 1: kryptera creadentials i en länkad tjänst</span><span class="sxs-lookup"><span data-stu-id="a901a-110">Example 1: Encrypt creadentials in a linked service</span></span>
```
PS C:\> New-AzureRmDataFactoryV2LinkedServiceEncryptCredential -ResourceGroupName resourceGroup -DataFactoryName myDataFactory -IntegrationRuntimeName myIR -File D:\sql.json
```

<span data-ttu-id="a901a-111">Det här kommandot krypterar autentiseringsuppgifter i fil D:\sql.jsmed integrerings programmet med namnet myIR.</span><span class="sxs-lookup"><span data-stu-id="a901a-111">This command encrypts credential in file D:\sql.json with the integration runtime named myIR.</span></span>

## <span data-ttu-id="a901a-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a901a-112">PARAMETERS</span></span>

### <span data-ttu-id="a901a-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="a901a-113">-DataFactory</span></span>
<span data-ttu-id="a901a-114">Data fabriks objekt.</span><span class="sxs-lookup"><span data-stu-id="a901a-114">The data factory object.</span></span>

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

### <span data-ttu-id="a901a-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="a901a-115">-DataFactoryName</span></span>
<span data-ttu-id="a901a-116">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="a901a-116">The data factory name.</span></span>

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

### <span data-ttu-id="a901a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a901a-117">-DefaultProfile</span></span>
<span data-ttu-id="a901a-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a901a-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a901a-119">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="a901a-119">-DefinitionFile</span></span>
<span data-ttu-id="a901a-120">Sökvägen till JSON-filen.</span><span class="sxs-lookup"><span data-stu-id="a901a-120">The JSON file path.</span></span>

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

### <span data-ttu-id="a901a-121">-Force</span><span class="sxs-lookup"><span data-stu-id="a901a-121">-Force</span></span>
<span data-ttu-id="a901a-122">Kör cmdleten utan att behöva bekräfta.</span><span class="sxs-lookup"><span data-stu-id="a901a-122">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="a901a-123">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="a901a-123">-IntegrationRuntimeName</span></span>
<span data-ttu-id="a901a-124">Integrerings körens namn.</span><span class="sxs-lookup"><span data-stu-id="a901a-124">The integration runtime name.</span></span>

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

### <span data-ttu-id="a901a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a901a-125">-ResourceGroupName</span></span>
<span data-ttu-id="a901a-126">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="a901a-126">The resource group name.</span></span>

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

### <span data-ttu-id="a901a-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a901a-127">-Confirm</span></span>
<span data-ttu-id="a901a-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a901a-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a901a-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a901a-129">-WhatIf</span></span>
<span data-ttu-id="a901a-130">Visar vad som händer om cmdleten körs men inte kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a901a-130">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="a901a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a901a-131">CommonParameters</span></span>
<span data-ttu-id="a901a-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a901a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a901a-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a901a-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a901a-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a901a-134">INPUTS</span></span>

### <span data-ttu-id="a901a-135">System. String</span><span class="sxs-lookup"><span data-stu-id="a901a-135">System.String</span></span>
<span data-ttu-id="a901a-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="a901a-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="a901a-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a901a-137">OUTPUTS</span></span>

### <span data-ttu-id="a901a-138">System. String</span><span class="sxs-lookup"><span data-stu-id="a901a-138">System.String</span></span>

## <span data-ttu-id="a901a-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a901a-139">NOTES</span></span>

## <span data-ttu-id="a901a-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a901a-140">RELATED LINKS</span></span>
