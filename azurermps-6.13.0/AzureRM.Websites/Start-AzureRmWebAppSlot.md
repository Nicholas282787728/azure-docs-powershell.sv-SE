---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 0FDDDEE1-CEAD-46DA-A7EB-EE477ED59749
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/start-azurermwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Start-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Start-AzureRmWebAppSlot.md
ms.openlocfilehash: 089711bacd6401b4c44683a159e43a92a56106d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573815"
---
# <span data-ttu-id="8463d-101">Start-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8463d-101">Start-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="8463d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8463d-102">SYNOPSIS</span></span>
<span data-ttu-id="8463d-103">Startar en Azure Web App-plats.</span><span class="sxs-lookup"><span data-stu-id="8463d-103">Starts an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8463d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8463d-104">SYNTAX</span></span>

### <span data-ttu-id="8463d-105">S</span><span class="sxs-lookup"><span data-stu-id="8463d-105">S1</span></span>
```
Start-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8463d-106">S2</span><span class="sxs-lookup"><span data-stu-id="8463d-106">S2</span></span>
```
Start-AzureRmWebAppSlot [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8463d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8463d-107">DESCRIPTION</span></span>
<span data-ttu-id="8463d-108">Cmdleten **Start-AzureRmWebAppSlot** startar en Azure Web App-plats.</span><span class="sxs-lookup"><span data-stu-id="8463d-108">The **Start-AzureRmWebAppSlot** cmdlet starts an Azure Web App Slot.</span></span>

## <span data-ttu-id="8463d-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8463d-109">EXAMPLES</span></span>

### <span data-ttu-id="8463d-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="8463d-110">Example 1</span></span>
```
PS C:\>Start-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="8463d-111">Det här kommandot startar facket som heter Slot001 som hör till webb programmet som heter ContosoWebApp och som tillhör resurs gruppen som heter default-West-väst.</span><span class="sxs-lookup"><span data-stu-id="8463d-111">This command starts the Slot named Slot001 pertaining to the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="8463d-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8463d-112">PARAMETERS</span></span>

### <span data-ttu-id="8463d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8463d-113">-DefaultProfile</span></span>
<span data-ttu-id="8463d-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8463d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8463d-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="8463d-115">-Name</span></span>
<span data-ttu-id="8463d-116">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="8463d-116">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8463d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8463d-117">-ResourceGroupName</span></span>
<span data-ttu-id="8463d-118">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="8463d-118">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8463d-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="8463d-119">-Slot</span></span>
<span data-ttu-id="8463d-120">WebApp-slot</span><span class="sxs-lookup"><span data-stu-id="8463d-120">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8463d-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="8463d-121">-WebApp</span></span>
<span data-ttu-id="8463d-122">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="8463d-122">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8463d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8463d-123">CommonParameters</span></span>
<span data-ttu-id="8463d-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8463d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8463d-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8463d-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8463d-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8463d-126">INPUTS</span></span>

### <span data-ttu-id="8463d-127">System. String</span><span class="sxs-lookup"><span data-stu-id="8463d-127">System.String</span></span>

### <span data-ttu-id="8463d-128">Microsoft. Azure. Management. webbplatser. Models. site</span><span class="sxs-lookup"><span data-stu-id="8463d-128">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="8463d-129">Parametrar: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8463d-129">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="8463d-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8463d-130">OUTPUTS</span></span>

### <span data-ttu-id="8463d-131">Microsoft. Azure. Management. webbplatser. Models. site</span><span class="sxs-lookup"><span data-stu-id="8463d-131">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="8463d-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8463d-132">NOTES</span></span>

## <span data-ttu-id="8463d-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8463d-133">RELATED LINKS</span></span>

[<span data-ttu-id="8463d-134">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8463d-134">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="8463d-135">New-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8463d-135">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="8463d-136">Remove-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8463d-136">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="8463d-137">Restart-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8463d-137">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="8463d-138">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8463d-138">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="8463d-139">Stopp-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8463d-139">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="8463d-140">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="8463d-140">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
