---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 0FDDDEE1-CEAD-46DA-A7EB-EE477ED59749
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/start-azurermwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Start-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Start-AzureRmWebAppSlot.md
ms.openlocfilehash: e9b0fa9f492c64f86668688d12171795735a46dd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573127"
---
# <span data-ttu-id="ae919-101">Start-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ae919-101">Start-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="ae919-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ae919-102">SYNOPSIS</span></span>
<span data-ttu-id="ae919-103">Startar en Azure Web App-plats.</span><span class="sxs-lookup"><span data-stu-id="ae919-103">Starts an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae919-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ae919-104">SYNTAX</span></span>

### <span data-ttu-id="ae919-105">S</span><span class="sxs-lookup"><span data-stu-id="ae919-105">S1</span></span>
```
Start-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae919-106">S2</span><span class="sxs-lookup"><span data-stu-id="ae919-106">S2</span></span>
```
Start-AzureRmWebAppSlot [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ae919-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ae919-107">DESCRIPTION</span></span>
<span data-ttu-id="ae919-108">Cmdleten **Start-AzureRmWebAppSlot** startar en Azure Web App-plats.</span><span class="sxs-lookup"><span data-stu-id="ae919-108">The **Start-AzureRmWebAppSlot** cmdlet starts an Azure Web App Slot.</span></span>

## <span data-ttu-id="ae919-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ae919-109">EXAMPLES</span></span>

### <span data-ttu-id="ae919-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ae919-110">Example 1</span></span>
```
PS C:\>Start-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="ae919-111">Det här kommandot startar facket som heter Slot001 som hör till webb programmet som heter ContosoWebApp och som tillhör resurs gruppen som heter default-West-väst.</span><span class="sxs-lookup"><span data-stu-id="ae919-111">This command starts the Slot named Slot001 pertaining to the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="ae919-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ae919-112">PARAMETERS</span></span>

### <span data-ttu-id="ae919-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae919-113">-DefaultProfile</span></span>
<span data-ttu-id="ae919-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ae919-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae919-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="ae919-115">-Name</span></span>
<span data-ttu-id="ae919-116">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="ae919-116">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae919-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae919-117">-ResourceGroupName</span></span>
<span data-ttu-id="ae919-118">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="ae919-118">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae919-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="ae919-119">-Slot</span></span>
<span data-ttu-id="ae919-120">WebApp-slot</span><span class="sxs-lookup"><span data-stu-id="ae919-120">WebApp Slot Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae919-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="ae919-121">-WebApp</span></span>
<span data-ttu-id="ae919-122">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="ae919-122">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ae919-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae919-123">CommonParameters</span></span>
<span data-ttu-id="ae919-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae919-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae919-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae919-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae919-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ae919-126">INPUTS</span></span>

### <span data-ttu-id="ae919-127">Webbplatsmallar</span><span class="sxs-lookup"><span data-stu-id="ae919-127">Site</span></span>
<span data-ttu-id="ae919-128">Parametern ' WebApp ' godkänner värdet av typen ' site ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="ae919-128">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="ae919-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ae919-129">OUTPUTS</span></span>

## <span data-ttu-id="ae919-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ae919-130">NOTES</span></span>

## <span data-ttu-id="ae919-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ae919-131">RELATED LINKS</span></span>

[<span data-ttu-id="ae919-132">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ae919-132">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="ae919-133">New-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ae919-133">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="ae919-134">Remove-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ae919-134">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="ae919-135">Restart-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ae919-135">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="ae919-136">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ae919-136">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="ae919-137">Stopp-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ae919-137">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="ae919-138">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="ae919-138">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
