---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: A87ED954-9C09-4329-A005-ABFF36C45E6E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebApp.md
ms.openlocfilehash: 64945cf503248fc0561dc894090c73d2d7151e4c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756306"
---
# <span data-ttu-id="b27a7-101">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="b27a7-101">Get-AzureRmWebApp</span></span>

## <span data-ttu-id="b27a7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b27a7-102">SYNOPSIS</span></span>
<span data-ttu-id="b27a7-103">Hämtar Azure Web Apps i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="b27a7-103">Gets Azure Web Apps in the specified resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b27a7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b27a7-104">SYNTAX</span></span>

### <span data-ttu-id="b27a7-105">S</span><span class="sxs-lookup"><span data-stu-id="b27a7-105">S1</span></span>
```
Get-AzureRmWebApp [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b27a7-106">S2</span><span class="sxs-lookup"><span data-stu-id="b27a7-106">S2</span></span>
```
Get-AzureRmWebApp [-AppServicePlan] <ServerFarmWithRichSku> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b27a7-107">S3</span><span class="sxs-lookup"><span data-stu-id="b27a7-107">S3</span></span>
```
Get-AzureRmWebApp [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b27a7-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b27a7-108">DESCRIPTION</span></span>
<span data-ttu-id="b27a7-109">Cmdleten **Get-AzureRmWebApp** hämtar information om en Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="b27a7-109">The **Get-AzureRmWebApp** cmdlet gets information about an Azure Web App.</span></span>

## <span data-ttu-id="b27a7-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b27a7-110">EXAMPLES</span></span>

### <span data-ttu-id="b27a7-111">Exempel 1: Hämta ett webb program från en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="b27a7-111">Example 1: Get a Web App from a resource group</span></span>
```
PS C:\>Get-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite" -SlotName "Slot001"
```

<span data-ttu-id="b27a7-112">Det här kommandot hämtar webb programmet som heter ContosoSite som tillhör resurs gruppens standard-väst.</span><span class="sxs-lookup"><span data-stu-id="b27a7-112">This command gets the Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="b27a7-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b27a7-113">PARAMETERS</span></span>

### <span data-ttu-id="b27a7-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="b27a7-114">-AppServicePlan</span></span>
<span data-ttu-id="b27a7-115">App Service plan-objekt</span><span class="sxs-lookup"><span data-stu-id="b27a7-115">App Service Plan object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b27a7-116">-Plats</span><span class="sxs-lookup"><span data-stu-id="b27a7-116">-Location</span></span>
<span data-ttu-id="b27a7-117">Plats</span><span class="sxs-lookup"><span data-stu-id="b27a7-117">Location</span></span>

```yaml
Type: System.String
Parameter Sets: S3
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b27a7-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="b27a7-118">-Name</span></span>
<span data-ttu-id="b27a7-119">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="b27a7-119">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b27a7-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b27a7-120">-ResourceGroupName</span></span>
<span data-ttu-id="b27a7-121">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="b27a7-121">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b27a7-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b27a7-122">-DefaultProfile</span></span>
<span data-ttu-id="b27a7-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b27a7-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b27a7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b27a7-124">CommonParameters</span></span>
<span data-ttu-id="b27a7-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b27a7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b27a7-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b27a7-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b27a7-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b27a7-127">INPUTS</span></span>

## <span data-ttu-id="b27a7-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b27a7-128">OUTPUTS</span></span>

## <span data-ttu-id="b27a7-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b27a7-129">NOTES</span></span>

## <span data-ttu-id="b27a7-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b27a7-130">RELATED LINKS</span></span>

[<span data-ttu-id="b27a7-131">New-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="b27a7-131">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="b27a7-132">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="b27a7-132">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="b27a7-133">Restart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="b27a7-133">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="b27a7-134">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="b27a7-134">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="b27a7-135">Stopp-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="b27a7-135">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


