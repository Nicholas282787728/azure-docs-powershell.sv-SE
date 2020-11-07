---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactorygatewayauthkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryGatewayAuthKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryGatewayAuthKey.md
ms.openlocfilehash: ed1cbf5fb39ba89427260225ecad0b4b8b5b1461
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744809"
---
# <span data-ttu-id="48b07-101">Get-AzDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="48b07-101">Get-AzDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="48b07-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="48b07-102">SYNOPSIS</span></span>
<span data-ttu-id="48b07-103">Hämtar Gateway-autentiseringsuppsättningen för en Azure Data fabrik.</span><span class="sxs-lookup"><span data-stu-id="48b07-103">Gets gateway auth key for an Azure Data Factory.</span></span>

## <span data-ttu-id="48b07-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="48b07-104">SYNTAX</span></span>

### <span data-ttu-id="48b07-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="48b07-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryGatewayAuthKey [-DataFactoryName] <String> [-GatewayName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="48b07-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="48b07-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryGatewayAuthKey [-InputObject] <PSDataFactory> [-GatewayName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="48b07-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="48b07-107">DESCRIPTION</span></span>
<span data-ttu-id="48b07-108">Cmdleten **Get-AzDataFactoryGatewayAuthKey** tar emot Gateway-autentiseringsuppsättningen för en angiven Azure Data Factory Gateway.</span><span class="sxs-lookup"><span data-stu-id="48b07-108">The **Get-AzDataFactoryGatewayAuthKey** cmdlet gets gateway auth key for a specified Azure Data Factory gateway.</span></span>
<span data-ttu-id="48b07-109">Du registrerar gatewayen med en moln tjänst genom att använda denna KEY1 eller key2.</span><span class="sxs-lookup"><span data-stu-id="48b07-109">You register the gateway with a cloud service by using this key1 or key2 of this auth key.</span></span>

## <span data-ttu-id="48b07-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="48b07-110">EXAMPLES</span></span>

### <span data-ttu-id="48b07-111">Exempel 1: hämtar en gateways autentiseringsprovider</span><span class="sxs-lookup"><span data-stu-id="48b07-111">Example 1: Gets auth key of a gateway</span></span>
```
PS C:\> Get-AzDataFactoryGatewayAuthKey -ResourceGroup ADFResource -GatewayName 'MyGateway' -DataFactoryName MyADF
Key1 : DMG@632e739e-1053-4070-9102-8591f067526e@41fcbc45-c594-4152-a8f1-fcbcd6452aea@wu@ZgBjjX6GfJcrzTQInEV9PoOqsDrqOmC
       gGHqUg1THLqA=
Key2 : DMG@632e739e-1053-4070-9102-8591f067526e@41fcbc45-c594-4152-a8f1-fcbcd6452aea@wu@kFXxBdFCEBeL7LPB3hA3LqLd1uNFbyv
       YmWxtV4WD3JQ=
```

<span data-ttu-id="48b07-112">Det här kommandot får Gateway-autentiseringsuppsättningen för data fabriks gatewayen med namnet min Gateway.</span><span class="sxs-lookup"><span data-stu-id="48b07-112">This command gets gateway auth key for the data factory gateway named MyGateway.</span></span>

## <span data-ttu-id="48b07-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="48b07-113">PARAMETERS</span></span>

### <span data-ttu-id="48b07-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="48b07-114">-DataFactoryName</span></span>
<span data-ttu-id="48b07-115">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="48b07-115">The data factory name.</span></span>

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

### <span data-ttu-id="48b07-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48b07-116">-DefaultProfile</span></span>
<span data-ttu-id="48b07-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="48b07-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="48b07-118">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="48b07-118">-GatewayName</span></span>
<span data-ttu-id="48b07-119">Data fabrikens Gateway-namn.</span><span class="sxs-lookup"><span data-stu-id="48b07-119">The data factory gateway name.</span></span>

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

### <span data-ttu-id="48b07-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="48b07-120">-InputObject</span></span>
<span data-ttu-id="48b07-121">Data fabriks objekt</span><span class="sxs-lookup"><span data-stu-id="48b07-121">The data factory object</span></span>

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

### <span data-ttu-id="48b07-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48b07-122">-ResourceGroupName</span></span>
<span data-ttu-id="48b07-123">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="48b07-123">The resource group name.</span></span>

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

### <span data-ttu-id="48b07-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48b07-124">CommonParameters</span></span>
<span data-ttu-id="48b07-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48b07-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48b07-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48b07-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48b07-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="48b07-127">INPUTS</span></span>

### <span data-ttu-id="48b07-128">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="48b07-128">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="48b07-129">System. String</span><span class="sxs-lookup"><span data-stu-id="48b07-129">System.String</span></span>

## <span data-ttu-id="48b07-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="48b07-130">OUTPUTS</span></span>

### <span data-ttu-id="48b07-131">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="48b07-131">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="48b07-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="48b07-132">NOTES</span></span>
* <span data-ttu-id="48b07-133">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="48b07-133">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="48b07-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="48b07-134">RELATED LINKS</span></span>

<span data-ttu-id="48b07-135">[New-AzDataFactoryGateway](./New-AzDataFactoryGateway.md) 
 [New-AzDataFactoryGatewayAuthKey](./New-AzDataFactoryGatewayAuthKey.md)</span><span class="sxs-lookup"><span data-stu-id="48b07-135">[New-AzDataFactoryGateway](./New-AzDataFactoryGateway.md)
[New-AzDataFactoryGatewayAuthKey](./New-AzDataFactoryGatewayAuthKey.md)</span></span>

