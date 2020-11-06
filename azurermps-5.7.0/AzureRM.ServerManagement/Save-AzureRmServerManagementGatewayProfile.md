---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM
ms.assetid: ECF85C07-2C9E-487D-A2ED-77875C380244
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servermanagement/save-azurermservermanagementgatewayprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Save-AzureRmServerManagementGatewayProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Save-AzureRmServerManagementGatewayProfile.md
ms.openlocfilehash: 8dd9aeaaf987fba155ca80b0c8739d44c80945e6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575506"
---
# <span data-ttu-id="7b36a-101">Save-AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="7b36a-101">Save-AzureRmServerManagementGatewayProfile</span></span>

## <span data-ttu-id="7b36a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7b36a-102">SYNOPSIS</span></span>
<span data-ttu-id="7b36a-103">Hämtar profilen för en server hanterings-gateway och sparar den i en lokal fil.</span><span class="sxs-lookup"><span data-stu-id="7b36a-103">Downloads the profile for a Server Management gateway and saves it to a local file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7b36a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7b36a-104">SYNTAX</span></span>

### <span data-ttu-id="7b36a-105">ByName</span><span class="sxs-lookup"><span data-stu-id="7b36a-105">ByName</span></span>
```
Save-AzureRmServerManagementGatewayProfile [-OutputFile] <FileInfo> [-ResourceGroupName] <String>
 [-GatewayName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7b36a-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="7b36a-106">ByObject</span></span>
```
Save-AzureRmServerManagementGatewayProfile [-OutputFile] <FileInfo> [-Gateway] <Gateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7b36a-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7b36a-107">DESCRIPTION</span></span>
<span data-ttu-id="7b36a-108">Cmdleten **Save-AzureRmServerManagementGatewayProfile** laddar ner profilen för en Azure Server Management Gateway och lagrar den i en lokal fil.</span><span class="sxs-lookup"><span data-stu-id="7b36a-108">The **Save-AzureRmServerManagementGatewayProfile** cmdlet downloads the profile for an Azure Server Management gateway and stores it to a local file.</span></span>

## <span data-ttu-id="7b36a-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7b36a-109">EXAMPLES</span></span>

## <span data-ttu-id="7b36a-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7b36a-110">PARAMETERS</span></span>

### <span data-ttu-id="7b36a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b36a-111">-DefaultProfile</span></span>
<span data-ttu-id="7b36a-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7b36a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7b36a-113">-Gateway</span><span class="sxs-lookup"><span data-stu-id="7b36a-113">-Gateway</span></span>
<span data-ttu-id="7b36a-114">Anger den gateway som denna cmdlet får profilen för.</span><span class="sxs-lookup"><span data-stu-id="7b36a-114">Specifies the gateway that this cmdlet gets the profile for.</span></span>

<span data-ttu-id="7b36a-115">Kan användas i stället för att ange ResourceGroupName och GatewayName</span><span class="sxs-lookup"><span data-stu-id="7b36a-115">May be used instead of specifying ResourceGroupName and GatewayName</span></span>

```yaml
Type: Gateway
Parameter Sets: ByObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7b36a-116">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="7b36a-116">-GatewayName</span></span>
<span data-ttu-id="7b36a-117">Anger namnet på den gateway som denna cmdlet får profilen för.</span><span class="sxs-lookup"><span data-stu-id="7b36a-117">Specifies the name of the gateway that this cmdlet gets the profile for.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b36a-118">-Utdatafil</span><span class="sxs-lookup"><span data-stu-id="7b36a-118">-OutputFile</span></span>
<span data-ttu-id="7b36a-119">Anger den lokala fil där profil data ska sparas.</span><span class="sxs-lookup"><span data-stu-id="7b36a-119">Specifies the local file in which to save the profile data.</span></span>

```yaml
Type: FileInfo
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b36a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b36a-120">-ResourceGroupName</span></span>
<span data-ttu-id="7b36a-121">Anger namnet på resurs gruppen som gatewayen tillhör.</span><span class="sxs-lookup"><span data-stu-id="7b36a-121">Specifies the name of the resource group that the gateway belongs to.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b36a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b36a-122">CommonParameters</span></span>
<span data-ttu-id="7b36a-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b36a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b36a-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b36a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b36a-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7b36a-125">INPUTS</span></span>

### <span data-ttu-id="7b36a-126">Portar</span><span class="sxs-lookup"><span data-stu-id="7b36a-126">Gateway</span></span>
<span data-ttu-id="7b36a-127">Parameter "Gateway" accepterar värdet för typen Gateway från pipeline</span><span class="sxs-lookup"><span data-stu-id="7b36a-127">Parameter 'Gateway' accepts value of type 'Gateway' from the pipeline</span></span>

## <span data-ttu-id="7b36a-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7b36a-128">OUTPUTS</span></span>

### <span data-ttu-id="7b36a-129">System. IO. FileInfo</span><span class="sxs-lookup"><span data-stu-id="7b36a-129">System.IO.FileInfo</span></span>

## <span data-ttu-id="7b36a-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7b36a-130">NOTES</span></span>

## <span data-ttu-id="7b36a-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7b36a-131">RELATED LINKS</span></span>

[<span data-ttu-id="7b36a-132">Install-AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="7b36a-132">Install-AzureRmServerManagementGatewayProfile</span></span>](./Install-AzureRmServerManagementGatewayProfile.md)

[<span data-ttu-id="7b36a-133">Reset-AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="7b36a-133">Reset-AzureRmServerManagementGatewayProfile</span></span>](./Reset-AzureRmServerManagementGatewayProfile.md)


