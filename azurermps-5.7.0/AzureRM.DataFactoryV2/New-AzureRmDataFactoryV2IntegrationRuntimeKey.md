---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/new-azurermdatafactoryv2integrationruntimekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/New-AzureRmDataFactoryV2IntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/New-AzureRmDataFactoryV2IntegrationRuntimeKey.md
ms.openlocfilehash: 2ac4868905ee1de93f87ecb17d6b9ced0f036cda
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573471"
---
# <span data-ttu-id="7cf14-101">New-AzureRmDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="7cf14-101">New-AzureRmDataFactoryV2IntegrationRuntimeKey</span></span>

## <span data-ttu-id="7cf14-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7cf14-102">SYNOPSIS</span></span>
<span data-ttu-id="7cf14-103">Återskapa den självvärdbaserade integrerings kör nyckeln.</span><span class="sxs-lookup"><span data-stu-id="7cf14-103">Regenerate self-hosted integration runtime key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7cf14-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7cf14-104">SYNTAX</span></span>

### <span data-ttu-id="7cf14-105">ByIntegrationRuntimeName (standard)</span><span class="sxs-lookup"><span data-stu-id="7cf14-105">ByIntegrationRuntimeName (Default)</span></span>
```
New-AzureRmDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-Name] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7cf14-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="7cf14-106">ByResourceId</span></span>
```
New-AzureRmDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7cf14-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="7cf14-107">ByIntegrationRuntimeObject</span></span>
```
New-AzureRmDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7cf14-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7cf14-108">DESCRIPTION</span></span>
<span data-ttu-id="7cf14-109">Cmdlet **New-AzureRmDataFactoryV2IntegrationRuntimeKey** återskapar integrerings körnings nyckeln med det nycklar som anges med parametern "värde namn".</span><span class="sxs-lookup"><span data-stu-id="7cf14-109">The cmdlet **New-AzureRmDataFactoryV2IntegrationRuntimeKey** regenerates the integration runtime key with the key name specified by 'KeyName' parameter.</span></span> <span data-ttu-id="7cf14-110">Den föregående knappen är ogiltig.</span><span class="sxs-lookup"><span data-stu-id="7cf14-110">The previous key will is invalid.</span></span>

## <span data-ttu-id="7cf14-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7cf14-111">EXAMPLES</span></span>

### <span data-ttu-id="7cf14-112">Exempel 1: skapa en ny-nyckeln för en integrations körning</span><span class="sxs-lookup"><span data-stu-id="7cf14-112">Example 1: Generate a new key for an integration runtime</span></span>
```
PS C:\> New-AzureRmDataFactoryV2IntegrationRuntimeKey -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' -KeyName authKey2

AuthKey1 AuthKey2
-------- --------
         IR@89895504-f647-48fd-8dd3-42fa556d67e3@***
```

<span data-ttu-id="7cf14-113">Cmdleten återskapar nyckeln ' authKey2 ' för integration runtime "test-selfhost-IR".</span><span class="sxs-lookup"><span data-stu-id="7cf14-113">The cmdlet regenerates key 'authKey2' for integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="7cf14-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7cf14-114">PARAMETERS</span></span>

### <span data-ttu-id="7cf14-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="7cf14-115">-DataFactoryName</span></span>
<span data-ttu-id="7cf14-116">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="7cf14-116">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cf14-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cf14-117">-DefaultProfile</span></span>
<span data-ttu-id="7cf14-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7cf14-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7cf14-119">-Force</span><span class="sxs-lookup"><span data-stu-id="7cf14-119">-Force</span></span>
<span data-ttu-id="7cf14-120">Kör cmdleten utan att behöva bekräfta.</span><span class="sxs-lookup"><span data-stu-id="7cf14-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="7cf14-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7cf14-121">-InputObject</span></span>
<span data-ttu-id="7cf14-122">Integration runtime-objekt.</span><span class="sxs-lookup"><span data-stu-id="7cf14-122">The integration runtime object.</span></span>

```yaml
Type: PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7cf14-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="7cf14-123">-KeyName</span></span>
<span data-ttu-id="7cf14-124">Namn på en autentiseringsnyckel för den självvärdbaserade integrerings körningen.</span><span class="sxs-lookup"><span data-stu-id="7cf14-124">The authentication key name of the self-hosted integration runtime.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: AuthKey1, AuthKey2

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cf14-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="7cf14-125">-Name</span></span>
<span data-ttu-id="7cf14-126">Integrerings körens namn.</span><span class="sxs-lookup"><span data-stu-id="7cf14-126">The integration runtime name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cf14-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7cf14-127">-ResourceGroupName</span></span>
<span data-ttu-id="7cf14-128">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="7cf14-128">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cf14-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7cf14-129">-ResourceId</span></span>
<span data-ttu-id="7cf14-130">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="7cf14-130">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cf14-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7cf14-131">-Confirm</span></span>
<span data-ttu-id="7cf14-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7cf14-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7cf14-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7cf14-133">-WhatIf</span></span>
<span data-ttu-id="7cf14-134">Visar vad som händer om cmdleten körs men inte kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7cf14-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="7cf14-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cf14-135">CommonParameters</span></span>
<span data-ttu-id="7cf14-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7cf14-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cf14-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7cf14-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cf14-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7cf14-138">INPUTS</span></span>

### <span data-ttu-id="7cf14-139">System. String</span><span class="sxs-lookup"><span data-stu-id="7cf14-139">System.String</span></span>
<span data-ttu-id="7cf14-140">Microsoft. Azure. commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="7cf14-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="7cf14-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7cf14-141">OUTPUTS</span></span>

### <span data-ttu-id="7cf14-142">Microsoft. Azure. commands. DataFactoryV2. Models. PSIntegrationRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="7cf14-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="7cf14-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7cf14-143">NOTES</span></span>

## <span data-ttu-id="7cf14-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7cf14-144">RELATED LINKS</span></span>

[<span data-ttu-id="7cf14-145">Get-AzureRmDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="7cf14-145">Get-AzureRmDataFactoryV2IntegrationRuntimeKey</span></span>]()