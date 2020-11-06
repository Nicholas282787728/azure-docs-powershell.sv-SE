---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 8546C3FE-5396-4027-BF33-F98F6C018A67
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryGatewayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryGatewayKey.md
ms.openlocfilehash: f1676d385b23711e71fbec5fb5d9131add4daaf4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577679"
---
# <span data-ttu-id="f411e-101">New-AzureRmDataFactoryGatewayKey</span><span class="sxs-lookup"><span data-stu-id="f411e-101">New-AzureRmDataFactoryGatewayKey</span></span>

## <span data-ttu-id="f411e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f411e-102">SYNOPSIS</span></span>
<span data-ttu-id="f411e-103">Skapar en gateway-sessionsnyckel för en Azure Data fabrik.</span><span class="sxs-lookup"><span data-stu-id="f411e-103">Creates a gateway key for an Azure Data Factory.</span></span> <span data-ttu-id="f411e-104">Denna cmdlet är föråldrad och du bör använda **New-AzureRmDataFactoryGatewayAuthKey** istället.</span><span class="sxs-lookup"><span data-stu-id="f411e-104">This cmdlet is deprecated, and you should use **New-AzureRmDataFactoryGatewayAuthKey** instead.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f411e-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f411e-105">SYNTAX</span></span>

### <span data-ttu-id="f411e-106">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="f411e-106">ByFactoryName (Default)</span></span>
```
New-AzureRmDataFactoryGatewayKey [-DataFactoryName] <String> [-GatewayName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f411e-107">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="f411e-107">ByFactoryObject</span></span>
```
New-AzureRmDataFactoryGatewayKey [-DataFactory] <PSDataFactory> [-GatewayName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f411e-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f411e-108">DESCRIPTION</span></span>
<span data-ttu-id="f411e-109">Cmdleten **New-AzureRmDataFactoryGatewayKey** skapar en gateway-sessionsnyckel för en angiven Azure Data Factory Gateway.</span><span class="sxs-lookup"><span data-stu-id="f411e-109">The **New-AzureRmDataFactoryGatewayKey** cmdlet creates a gateway key for a specified Azure Data Factory gateway.</span></span>
<span data-ttu-id="f411e-110">Du registrerar gatewayen med en moln tjänst med den här nyckeln.</span><span class="sxs-lookup"><span data-stu-id="f411e-110">You register the gateway with a cloud service by using this key.</span></span> <span data-ttu-id="f411e-111">Denna cmdlet är föråldrad och du bör använda **New-AzureRmDataFactoryGatewayAuthKey** istället.</span><span class="sxs-lookup"><span data-stu-id="f411e-111">This cmdlet is deprecated, and you should use **New-AzureRmDataFactoryGatewayAuthKey** instead.</span></span>

## <span data-ttu-id="f411e-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f411e-112">EXAMPLES</span></span>

### <span data-ttu-id="f411e-113">Exempel 1: skapa en gateway-nyckeln</span><span class="sxs-lookup"><span data-stu-id="f411e-113">Example 1: Create a gateway key</span></span>
```
PS C:\>New-AzureRmDataFactoryGatewayKey -ResourceGroupName "ADF" -GatewayName "ContosoGateway" -DataFactoryName "WikiADF" | Format-List
GatewayKey : ADF#40cbb3d9-2736-4794-a8a6-e6b839b4894f@a2d875ce-c9d7-4b8b-ad65-dd3ebbb9a940@8c0d1801-e863-44af-82e6-fb2f0c00f2ae@xz#Y9R0NhAeH3u7wgnrJyiWj4Y/QIhH4fFilIdzZgwsVQA=
```

<span data-ttu-id="f411e-114">Det här kommandot skapar en gateway-nyckeln för data fabriks-gatewayen med namnet ContosoGateway och skickar sedan Gateway-nyckeln till Format-List cmdlet med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="f411e-114">This command creates a gateway key for the data factory gateway named ContosoGateway, and then passes the gateway key to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="f411e-115">Om du vill ha mer information skriver du `Get-Help Format-List` .</span><span class="sxs-lookup"><span data-stu-id="f411e-115">For more information, type `Get-Help Format-List`.</span></span>

## <span data-ttu-id="f411e-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f411e-116">PARAMETERS</span></span>

### <span data-ttu-id="f411e-117">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="f411e-117">-DataFactory</span></span>
<span data-ttu-id="f411e-118">Anger ett **PSDataFactory** -objekt.</span><span class="sxs-lookup"><span data-stu-id="f411e-118">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="f411e-119">Denna cmdlet skapar en gateway-nyckeln för data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="f411e-119">This cmdlet creates a gateway key for the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f411e-120">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="f411e-120">-DataFactoryName</span></span>
<span data-ttu-id="f411e-121">Anger namnet på en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="f411e-121">Specifies the name of a data factory.</span></span>
<span data-ttu-id="f411e-122">Denna cmdlet skapar en gateway-nyckeln för data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="f411e-122">This cmdlet creates a gateway key for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="f411e-123">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="f411e-123">-GatewayName</span></span>
<span data-ttu-id="f411e-124">Anger namnet på gatewayen.</span><span class="sxs-lookup"><span data-stu-id="f411e-124">Specifies the name of the gateway.</span></span>
<span data-ttu-id="f411e-125">Denna cmdlet skapar en nyckeln för den gateway som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="f411e-125">This cmdlet creates a key for the gateway that this parameter specifies.</span></span>

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

### <span data-ttu-id="f411e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f411e-126">-ResourceGroupName</span></span>
<span data-ttu-id="f411e-127">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="f411e-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="f411e-128">Denna cmdlet skapar en nyckeln för en gateway som tillhör gruppen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="f411e-128">This cmdlet creates a key for a gateway that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="f411e-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f411e-129">-DefaultProfile</span></span>
<span data-ttu-id="f411e-130">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f411e-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f411e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f411e-131">CommonParameters</span></span>
<span data-ttu-id="f411e-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f411e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f411e-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f411e-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f411e-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f411e-134">INPUTS</span></span>

## <span data-ttu-id="f411e-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f411e-135">OUTPUTS</span></span>

### <span data-ttu-id="f411e-136">Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryGatewayKey</span><span class="sxs-lookup"><span data-stu-id="f411e-136">Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryGatewayKey</span></span>

## <span data-ttu-id="f411e-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f411e-137">NOTES</span></span>
* <span data-ttu-id="f411e-138">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="f411e-138">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="f411e-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f411e-139">RELATED LINKS</span></span>

<span data-ttu-id="f411e-140">[New-AzureRmDataFactoryGateway](./New-AzureRmDataFactoryGateway.md) 
 [Get-AzureRmDataFactoryGatewayAuthKey](./Get-AzureRmDataFactoryGatewayAuthKey.md) 
 [New-AzureRmDataFactoryGatewayAuthKey](./New-AzureRmDataFactoryGatewayAuthKey.md)</span><span class="sxs-lookup"><span data-stu-id="f411e-140">[New-AzureRmDataFactoryGateway](./New-AzureRmDataFactoryGateway.md)
[Get-AzureRmDataFactoryGatewayAuthKey](./Get-AzureRmDataFactoryGatewayAuthKey.md)
[New-AzureRmDataFactoryGatewayAuthKey](./New-AzureRmDataFactoryGatewayAuthKey.md)</span></span>


