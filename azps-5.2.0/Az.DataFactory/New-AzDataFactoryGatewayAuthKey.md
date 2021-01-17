---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactorygatewayauthkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryGatewayAuthKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryGatewayAuthKey.md
ms.openlocfilehash: 541cedecbad563be3e1a016dd651d3e93af44d1e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98388683"
---
# <span data-ttu-id="9577d-101">New-AzDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="9577d-101">New-AzDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="9577d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9577d-102">SYNOPSIS</span></span>
<span data-ttu-id="9577d-103">Skapar en aukt-sessionsnyckel för en Azure Data Factory Gateway.</span><span class="sxs-lookup"><span data-stu-id="9577d-103">Creates auth key for an Azure Data Factory Gateway.</span></span>

## <span data-ttu-id="9577d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9577d-104">SYNTAX</span></span>

### <span data-ttu-id="9577d-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="9577d-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryGatewayAuthKey [-DataFactoryName] <String> [-GatewayName] <String> [-KeyName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9577d-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="9577d-106">ByFactoryObject</span></span>
```
New-AzDataFactoryGatewayAuthKey [-InputObject] <PSDataFactory> [-GatewayName] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9577d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9577d-107">DESCRIPTION</span></span>
<span data-ttu-id="9577d-108">Cmdleten **New-AzDataFactoryGatewayAuthKey** skapar Gateway-autentiseringsuppsättningen för en angiven Azure Data Factory Gateway.</span><span class="sxs-lookup"><span data-stu-id="9577d-108">The **New-AzDataFactoryGatewayAuthKey** cmdlet creates gateway auth key for a specified Azure Data Factory gateway.</span></span>
<span data-ttu-id="9577d-109">Du registrerar gatewayen med en moln tjänst med den här nyckeln.</span><span class="sxs-lookup"><span data-stu-id="9577d-109">You register the gateway with a cloud service by using this key.</span></span>

## <span data-ttu-id="9577d-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9577d-110">EXAMPLES</span></span>

### <span data-ttu-id="9577d-111">Exempel 1: skapar en gateway-autentiseringsprovider för KEY1</span><span class="sxs-lookup"><span data-stu-id="9577d-111">Example 1: Creates a gateway auth key for Key1</span></span>
```
PS C:\> New-AzDataFactoryGatewayAuthKey -ResourceGroup ADFResource -GatewayName 'MyGateway' -DataFactoryName MyADF -KeyName key1
Key1 : DMG@632e739e-1053-4070-9102-8591f067526e@41fcbc45-c594-4152-a8f1-fcbcd6452aea@wu@BH0EV9hu/o2IYGQzfYYD203XhdS6Tty
       fkYwYFbG6wBU=
Key2 :
```

<span data-ttu-id="9577d-112">Det här kommandot skapar en gateway-autentiseringsprovider för KEY1 för data fabriks-gatewayen med namnet min Gateway.</span><span class="sxs-lookup"><span data-stu-id="9577d-112">This command creates a gateway auth key of Key1 for the data factory gateway named MyGateway.</span></span>

## <span data-ttu-id="9577d-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9577d-113">PARAMETERS</span></span>

### <span data-ttu-id="9577d-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="9577d-114">-DataFactoryName</span></span>
<span data-ttu-id="9577d-115">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="9577d-115">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9577d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9577d-116">-DefaultProfile</span></span>
<span data-ttu-id="9577d-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="9577d-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9577d-118">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="9577d-118">-GatewayName</span></span>
<span data-ttu-id="9577d-119">Data fabrikens Gateway-namn.</span><span class="sxs-lookup"><span data-stu-id="9577d-119">The data factory gateway name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9577d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9577d-120">-InputObject</span></span>
<span data-ttu-id="9577d-121">Data fabriks objekt</span><span class="sxs-lookup"><span data-stu-id="9577d-121">The data factory object</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: DataFactory

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9577d-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="9577d-122">-KeyName</span></span>
<span data-ttu-id="9577d-123">Namnet på den gateway-autentiseringsprovider som ska återskapas, antingen "KEY1" eller "key2".</span><span class="sxs-lookup"><span data-stu-id="9577d-123">The name of gateway auth key to be regenerated, either 'key1' or 'key2'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: key1, key2

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9577d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9577d-124">-ResourceGroupName</span></span>
<span data-ttu-id="9577d-125">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="9577d-125">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9577d-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9577d-126">-Confirm</span></span>
<span data-ttu-id="9577d-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9577d-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9577d-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9577d-128">-WhatIf</span></span>
<span data-ttu-id="9577d-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9577d-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9577d-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9577d-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9577d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9577d-131">CommonParameters</span></span>
<span data-ttu-id="9577d-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9577d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9577d-133">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9577d-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9577d-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9577d-134">INPUTS</span></span>

### <span data-ttu-id="9577d-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="9577d-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="9577d-136">System. String</span><span class="sxs-lookup"><span data-stu-id="9577d-136">System.String</span></span>

## <span data-ttu-id="9577d-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9577d-137">OUTPUTS</span></span>

### <span data-ttu-id="9577d-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="9577d-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="9577d-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9577d-139">NOTES</span></span>
* <span data-ttu-id="9577d-140">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="9577d-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="9577d-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9577d-141">RELATED LINKS</span></span>

<span data-ttu-id="9577d-142">[New-AzDataFactoryGateway](./New-AzDataFactoryGateway.md) 
 [Get-AzDataFactoryGatewayAuthKey](./Get-AzDataFactoryGatewayAuthKey.md)</span><span class="sxs-lookup"><span data-stu-id="9577d-142">[New-AzDataFactoryGateway](./New-AzDataFactoryGateway.md)
[Get-AzDataFactoryGatewayAuthKey](./Get-AzDataFactoryGatewayAuthKey.md)</span></span>

