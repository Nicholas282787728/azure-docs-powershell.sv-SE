---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: ECF85C07-2C9E-487D-A2ED-77875C380244
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Save-AzureRmServerManagementGatewayProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Save-AzureRmServerManagementGatewayProfile.md
ms.openlocfilehash: af7184b3e43d2016ff4acc9e7634f831945a8fdf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582191"
---
# <span data-ttu-id="692bc-101">Save-AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="692bc-101">Save-AzureRmServerManagementGatewayProfile</span></span>

## <span data-ttu-id="692bc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="692bc-102">SYNOPSIS</span></span>
<span data-ttu-id="692bc-103">Hämtar profilen för en server hanterings-gateway och sparar den i en lokal fil.</span><span class="sxs-lookup"><span data-stu-id="692bc-103">Downloads the profile for a Server Management gateway and saves it to a local file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="692bc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="692bc-104">SYNTAX</span></span>

### <span data-ttu-id="692bc-105">ByName</span><span class="sxs-lookup"><span data-stu-id="692bc-105">ByName</span></span>
```
Save-AzureRmServerManagementGatewayProfile [-OutputFile] <FileInfo> [-ResourceGroupName] <String>
 [-GatewayName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="692bc-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="692bc-106">ByObject</span></span>
```
Save-AzureRmServerManagementGatewayProfile [-OutputFile] <FileInfo> [-Gateway] <Gateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="692bc-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="692bc-107">DESCRIPTION</span></span>
<span data-ttu-id="692bc-108">Cmdleten **Save-AzureRmServerManagementGatewayProfile** laddar ner profilen för en Azure Server Management Gateway och lagrar den i en lokal fil.</span><span class="sxs-lookup"><span data-stu-id="692bc-108">The **Save-AzureRmServerManagementGatewayProfile** cmdlet downloads the profile for an Azure Server Management gateway and stores it to a local file.</span></span>

## <span data-ttu-id="692bc-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="692bc-109">EXAMPLES</span></span>

## <span data-ttu-id="692bc-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="692bc-110">PARAMETERS</span></span>

### <span data-ttu-id="692bc-111">-Gateway</span><span class="sxs-lookup"><span data-stu-id="692bc-111">-Gateway</span></span>
<span data-ttu-id="692bc-112">Anger den gateway som denna cmdlet får profilen för.</span><span class="sxs-lookup"><span data-stu-id="692bc-112">Specifies the gateway that this cmdlet gets the profile for.</span></span>

<span data-ttu-id="692bc-113">Kan användas i stället för att ange ResourceGroupName och GatewayName</span><span class="sxs-lookup"><span data-stu-id="692bc-113">May be used instead of specifying ResourceGroupName and GatewayName</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServerManagement.Model.Gateway
Parameter Sets: ByObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="692bc-114">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="692bc-114">-GatewayName</span></span>
<span data-ttu-id="692bc-115">Anger namnet på den gateway som denna cmdlet får profilen för.</span><span class="sxs-lookup"><span data-stu-id="692bc-115">Specifies the name of the gateway that this cmdlet gets the profile for.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="692bc-116">-Utdatafil</span><span class="sxs-lookup"><span data-stu-id="692bc-116">-OutputFile</span></span>
<span data-ttu-id="692bc-117">Anger den lokala fil där profil data ska sparas.</span><span class="sxs-lookup"><span data-stu-id="692bc-117">Specifies the local file in which to save the profile data.</span></span>

```yaml
Type: System.IO.FileInfo
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="692bc-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="692bc-118">-ResourceGroupName</span></span>
<span data-ttu-id="692bc-119">Anger namnet på resurs gruppen som gatewayen tillhör.</span><span class="sxs-lookup"><span data-stu-id="692bc-119">Specifies the name of the resource group that the gateway belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="692bc-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="692bc-120">-DefaultProfile</span></span>
<span data-ttu-id="692bc-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="692bc-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="692bc-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="692bc-122">CommonParameters</span></span>
<span data-ttu-id="692bc-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="692bc-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="692bc-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="692bc-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="692bc-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="692bc-125">INPUTS</span></span>

### <span data-ttu-id="692bc-126">Portar</span><span class="sxs-lookup"><span data-stu-id="692bc-126">Gateway</span></span>
<span data-ttu-id="692bc-127">Parameter "Gateway" accepterar värdet för typen Gateway från pipeline</span><span class="sxs-lookup"><span data-stu-id="692bc-127">Parameter 'Gateway' accepts value of type 'Gateway' from the pipeline</span></span>

## <span data-ttu-id="692bc-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="692bc-128">OUTPUTS</span></span>

### <span data-ttu-id="692bc-129">System. IO. FileInfo</span><span class="sxs-lookup"><span data-stu-id="692bc-129">System.IO.FileInfo</span></span>

## <span data-ttu-id="692bc-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="692bc-130">NOTES</span></span>

## <span data-ttu-id="692bc-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="692bc-131">RELATED LINKS</span></span>

[<span data-ttu-id="692bc-132">Install-AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="692bc-132">Install-AzureRmServerManagementGatewayProfile</span></span>](./Install-AzureRmServerManagementGatewayProfile.md)

[<span data-ttu-id="692bc-133">Reset-AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="692bc-133">Reset-AzureRmServerManagementGatewayProfile</span></span>](./Reset-AzureRmServerManagementGatewayProfile.md)


