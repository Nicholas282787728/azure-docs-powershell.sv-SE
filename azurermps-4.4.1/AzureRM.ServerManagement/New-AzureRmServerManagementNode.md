---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: CEA14FAB-4B57-48F2-938C-E3AD4AAAE753
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementNode.md
ms.openlocfilehash: e77059b94f9311caf25b58f2d626f0cafc4657e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577451"
---
# <span data-ttu-id="10308-101">New-AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="10308-101">New-AzureRmServerManagementNode</span></span>

## <span data-ttu-id="10308-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="10308-102">SYNOPSIS</span></span>
<span data-ttu-id="10308-103">Skapar en server hanterings nod.</span><span class="sxs-lookup"><span data-stu-id="10308-103">Creates a Server Management node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="10308-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="10308-104">SYNTAX</span></span>

### <span data-ttu-id="10308-105">ByName</span><span class="sxs-lookup"><span data-stu-id="10308-105">ByName</span></span>
```
New-AzureRmServerManagementNode [-ResourceGroupName] <String> [-GatewayName] <String> [-Location] <String>
 -NodeName <String> [-ComputerName <String>] -Credential <PSCredential> [-Tags <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="10308-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="10308-106">ByObject</span></span>
```
New-AzureRmServerManagementNode [-Gateway] <Gateway> -NodeName <String> [-ComputerName <String>]
 -Credential <PSCredential> [-Tags <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10308-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="10308-107">DESCRIPTION</span></span>
<span data-ttu-id="10308-108">Cmdleten **New-AzureRmServerManagementNode** skapar en Azure Server Management-nod.</span><span class="sxs-lookup"><span data-stu-id="10308-108">The **New-AzureRmServerManagementNode** cmdlet creates an Azure Server Management node.</span></span>

## <span data-ttu-id="10308-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="10308-109">EXAMPLES</span></span>

## <span data-ttu-id="10308-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="10308-110">PARAMETERS</span></span>

### <span data-ttu-id="10308-111">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="10308-111">-ComputerName</span></span>
<span data-ttu-id="10308-112">Anger dator namnet på den dator som hanteras.</span><span class="sxs-lookup"><span data-stu-id="10308-112">Specifies the computer name of the computer that is being managed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10308-113">-Autentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="10308-113">-Credential</span></span>
<span data-ttu-id="10308-114">Anger ett **PSCredential** -objekt för anslutningen till noden Server Management.</span><span class="sxs-lookup"><span data-stu-id="10308-114">Specifies a **PSCredential** object for the connection to the Server Management Node.</span></span>
<span data-ttu-id="10308-115">Använd cmdleten Get-Credential för att hämta ett Credential-objekt.</span><span class="sxs-lookup"><span data-stu-id="10308-115">To obtain a credential object, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="10308-116">Om du vill ha mer information skriver du `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="10308-116">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10308-117">-Gateway</span><span class="sxs-lookup"><span data-stu-id="10308-117">-Gateway</span></span>
<span data-ttu-id="10308-118">Anger den gateway som hanterar noden.</span><span class="sxs-lookup"><span data-stu-id="10308-118">Specifies the gateway that manages the node.</span></span>

<span data-ttu-id="10308-119">Den här parametern kan användas i stället för parametrarna *ResourceGroupName* , *GatewayName* och *location* .</span><span class="sxs-lookup"><span data-stu-id="10308-119">This parameter can be used instead of the *ResourceGroupName* , *GatewayName* , and *Location* parameters.</span></span>

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

### <span data-ttu-id="10308-120">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="10308-120">-GatewayName</span></span>
<span data-ttu-id="10308-121">Anger namnet på den gateway som använder noden.</span><span class="sxs-lookup"><span data-stu-id="10308-121">Specifies the name of the gateway that accesses the node.</span></span>

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

### <span data-ttu-id="10308-122">-Plats</span><span class="sxs-lookup"><span data-stu-id="10308-122">-Location</span></span>
<span data-ttu-id="10308-123">Anger den plats där den här cmdleten skapar noden.</span><span class="sxs-lookup"><span data-stu-id="10308-123">Specifies the location in which this cmdlet creates the node.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10308-124">-Nodnamn</span><span class="sxs-lookup"><span data-stu-id="10308-124">-NodeName</span></span>
<span data-ttu-id="10308-125">Anger namnet på noden.</span><span class="sxs-lookup"><span data-stu-id="10308-125">Specifies the name of the node.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10308-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10308-126">-ResourceGroupName</span></span>
<span data-ttu-id="10308-127">Anger namnet på den resurs grupp som cmdleten skapar noden för.</span><span class="sxs-lookup"><span data-stu-id="10308-127">Specifies the name of the resource group in which this cmdlet creates the node.</span></span>

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

### <span data-ttu-id="10308-128">-Taggar</span><span class="sxs-lookup"><span data-stu-id="10308-128">-Tags</span></span>
<span data-ttu-id="10308-129">Anger taggar som par med nyckelord.</span><span class="sxs-lookup"><span data-stu-id="10308-129">Specifies tags as key-value pairs.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10308-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10308-130">-DefaultProfile</span></span>
<span data-ttu-id="10308-131">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="10308-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="10308-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10308-132">CommonParameters</span></span>
<span data-ttu-id="10308-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10308-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10308-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10308-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10308-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="10308-135">INPUTS</span></span>

### <span data-ttu-id="10308-136">Portar</span><span class="sxs-lookup"><span data-stu-id="10308-136">Gateway</span></span>
<span data-ttu-id="10308-137">Parameter "Gateway" accepterar värdet för typen Gateway från pipeline</span><span class="sxs-lookup"><span data-stu-id="10308-137">Parameter 'Gateway' accepts value of type 'Gateway' from the pipeline</span></span>

## <span data-ttu-id="10308-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="10308-138">OUTPUTS</span></span>

### <span data-ttu-id="10308-139">Microsoft. Azure. commands. ServerManagement. Model. Node</span><span class="sxs-lookup"><span data-stu-id="10308-139">Microsoft.Azure.Commands.ServerManagement.Model.Node</span></span>

## <span data-ttu-id="10308-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="10308-140">NOTES</span></span>

## <span data-ttu-id="10308-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="10308-141">RELATED LINKS</span></span>

[<span data-ttu-id="10308-142">Get-AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="10308-142">Get-AzureRmServerManagementNode</span></span>](./Get-AzureRmServerManagementNode.md)

[<span data-ttu-id="10308-143">Remove-AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="10308-143">Remove-AzureRmServerManagementNode</span></span>](./Remove-AzureRmServerManagementNode.md)


