---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 0FDDDEE1-CEAD-46DA-A7EB-EE477ED59749
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Start-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Start-AzureRmWebAppSlot.md
ms.openlocfilehash: 687adf3cd7101a9747346c4b1aa3ba201d6dcc46
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573597"
---
# <span data-ttu-id="f2517-101">Start-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f2517-101">Start-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="f2517-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f2517-102">SYNOPSIS</span></span>
<span data-ttu-id="f2517-103">Startar en Azure Web App-plats.</span><span class="sxs-lookup"><span data-stu-id="f2517-103">Starts an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f2517-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f2517-104">SYNTAX</span></span>

### <span data-ttu-id="f2517-105">S</span><span class="sxs-lookup"><span data-stu-id="f2517-105">S1</span></span>
```
Start-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f2517-106">S2</span><span class="sxs-lookup"><span data-stu-id="f2517-106">S2</span></span>
```
Start-AzureRmWebAppSlot [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2517-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f2517-107">DESCRIPTION</span></span>
<span data-ttu-id="f2517-108">Cmdleten **Start-AzureRmWebAppSlot** startar en Azure Web App-plats.</span><span class="sxs-lookup"><span data-stu-id="f2517-108">The **Start-AzureRmWebAppSlot** cmdlet starts an Azure Web App Slot.</span></span>

## <span data-ttu-id="f2517-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f2517-109">EXAMPLES</span></span>

### <span data-ttu-id="f2517-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f2517-110">Example 1</span></span>
```
PS C:\>Start-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="f2517-111">Det här kommandot startar facket som heter Slot001 som hör till webb programmet som heter ContosoWebApp och som tillhör resurs gruppen som heter default-West-väst.</span><span class="sxs-lookup"><span data-stu-id="f2517-111">This command starts the Slot named Slot001 pertaining to the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="f2517-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f2517-112">PARAMETERS</span></span>

### <span data-ttu-id="f2517-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="f2517-113">-Name</span></span>
<span data-ttu-id="f2517-114">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="f2517-114">WebApp Name</span></span>

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

### <span data-ttu-id="f2517-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2517-115">-ResourceGroupName</span></span>
<span data-ttu-id="f2517-116">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="f2517-116">Resource Group Name</span></span>

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

### <span data-ttu-id="f2517-117">-Plats</span><span class="sxs-lookup"><span data-stu-id="f2517-117">-Slot</span></span>
<span data-ttu-id="f2517-118">WebApp-slot</span><span class="sxs-lookup"><span data-stu-id="f2517-118">WebApp Slot Name</span></span>

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

### <span data-ttu-id="f2517-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="f2517-119">-WebApp</span></span>
<span data-ttu-id="f2517-120">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="f2517-120">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f2517-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2517-121">-DefaultProfile</span></span>
<span data-ttu-id="f2517-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f2517-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f2517-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2517-123">CommonParameters</span></span>
<span data-ttu-id="f2517-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2517-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2517-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2517-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2517-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f2517-126">INPUTS</span></span>

### <span data-ttu-id="f2517-127">Webbplatsmallar</span><span class="sxs-lookup"><span data-stu-id="f2517-127">Site</span></span>
<span data-ttu-id="f2517-128">Parametern ' WebApp ' godkänner värdet av typen ' site ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="f2517-128">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="f2517-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f2517-129">OUTPUTS</span></span>

## <span data-ttu-id="f2517-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f2517-130">NOTES</span></span>

## <span data-ttu-id="f2517-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f2517-131">RELATED LINKS</span></span>

[<span data-ttu-id="f2517-132">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f2517-132">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="f2517-133">New-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f2517-133">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="f2517-134">Remove-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f2517-134">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="f2517-135">Restart-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f2517-135">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="f2517-136">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f2517-136">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="f2517-137">Stopp-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f2517-137">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="f2517-138">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="f2517-138">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
