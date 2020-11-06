---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: A87ED954-9C09-4329-A005-ABFF36C45E6E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebApp.md
ms.openlocfilehash: 83afdb179a9c0f135fd17827ff59f89ad117e3b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577760"
---
# <span data-ttu-id="92286-101">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="92286-101">Get-AzureRmWebApp</span></span>

## <span data-ttu-id="92286-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="92286-102">SYNOPSIS</span></span>
<span data-ttu-id="92286-103">Hämtar Azure Web Apps i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="92286-103">Gets Azure Web Apps in the specified resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="92286-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="92286-104">SYNTAX</span></span>

### <span data-ttu-id="92286-105">S</span><span class="sxs-lookup"><span data-stu-id="92286-105">S1</span></span>
```
Get-AzureRmWebApp [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="92286-106">S2</span><span class="sxs-lookup"><span data-stu-id="92286-106">S2</span></span>
```
Get-AzureRmWebApp [-AppServicePlan] <PSAppServicePlan> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="92286-107">S3</span><span class="sxs-lookup"><span data-stu-id="92286-107">S3</span></span>
```
Get-AzureRmWebApp [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="92286-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="92286-108">DESCRIPTION</span></span>
<span data-ttu-id="92286-109">Cmdleten **Get-AzureRmWebApp** hämtar information om en Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="92286-109">The **Get-AzureRmWebApp** cmdlet gets information about an Azure Web App.</span></span>

## <span data-ttu-id="92286-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="92286-110">EXAMPLES</span></span>

### <span data-ttu-id="92286-111">Exempel 1: Hämta ett webb program från en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="92286-111">Example 1: Get a Web App from a resource group</span></span>
```
PS C:\>Get-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="92286-112">Det här kommandot hämtar webb programmet som heter ContosoSite som tillhör resurs gruppens standard-väst.</span><span class="sxs-lookup"><span data-stu-id="92286-112">This command gets the Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="92286-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="92286-113">PARAMETERS</span></span>

### <span data-ttu-id="92286-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="92286-114">-AppServicePlan</span></span>
<span data-ttu-id="92286-115">App Service plan-objekt</span><span class="sxs-lookup"><span data-stu-id="92286-115">App Service Plan object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92286-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92286-116">-DefaultProfile</span></span>
<span data-ttu-id="92286-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="92286-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="92286-118">-Plats</span><span class="sxs-lookup"><span data-stu-id="92286-118">-Location</span></span>
<span data-ttu-id="92286-119">Plats</span><span class="sxs-lookup"><span data-stu-id="92286-119">Location</span></span>

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

### <span data-ttu-id="92286-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="92286-120">-Name</span></span>
<span data-ttu-id="92286-121">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="92286-121">WebApp Name</span></span>

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

### <span data-ttu-id="92286-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92286-122">-ResourceGroupName</span></span>
<span data-ttu-id="92286-123">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="92286-123">Resource Group Name</span></span>

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

### <span data-ttu-id="92286-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92286-124">CommonParameters</span></span>
<span data-ttu-id="92286-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92286-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92286-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92286-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92286-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="92286-127">INPUTS</span></span>

### <span data-ttu-id="92286-128">System. String</span><span class="sxs-lookup"><span data-stu-id="92286-128">System.String</span></span>

## <span data-ttu-id="92286-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="92286-129">OUTPUTS</span></span>

### <span data-ttu-id="92286-130">Microsoft. Azure. Management. webbplatser. Models. site</span><span class="sxs-lookup"><span data-stu-id="92286-130">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="92286-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="92286-131">NOTES</span></span>

## <span data-ttu-id="92286-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="92286-132">RELATED LINKS</span></span>

[<span data-ttu-id="92286-133">New-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="92286-133">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="92286-134">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="92286-134">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="92286-135">Restart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="92286-135">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="92286-136">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="92286-136">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="92286-137">Stopp-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="92286-137">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


