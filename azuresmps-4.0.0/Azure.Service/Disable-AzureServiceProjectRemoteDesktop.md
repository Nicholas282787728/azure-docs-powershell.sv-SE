---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E735FCE5-D82F-42D0-8D74-6A568E55AC17
online version: ''
schema: 2.0.0
ms.openlocfilehash: 433a50a93f8fa8e68021d09d5c1ae464703e227c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093422"
---
# <span data-ttu-id="00690-101">Disable-AzureServiceProjectRemoteDesktop</span><span class="sxs-lookup"><span data-stu-id="00690-101">Disable-AzureServiceProjectRemoteDesktop</span></span>

## <span data-ttu-id="00690-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="00690-102">SYNOPSIS</span></span>
<span data-ttu-id="00690-103">Inaktiverar åtkomst till fjärr skrivbord till en moln tjänst.</span><span class="sxs-lookup"><span data-stu-id="00690-103">Disables Remote Desktop access to a cloud service.</span></span>

## <span data-ttu-id="00690-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="00690-104">SYNTAX</span></span>

```
Disable-AzureServiceProjectRemoteDesktop [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="00690-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="00690-105">DESCRIPTION</span></span>
<span data-ttu-id="00690-106">I det här avsnittet beskrivs cmdleten i 0.8.10-versionen av Microsoft Azure PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="00690-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="00690-107">För att få den version av modulen du använder, gå till Azure PowerShell-konsolen och skriv `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="00690-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="00690-108">**Disable-AzureServiceProjectRemoteDesktop** inaktiverar åtkomst till fjärr skrivbord till en värdbaserad tjänst.</span><span class="sxs-lookup"><span data-stu-id="00690-108">The **Disable-AzureServiceProjectRemoteDesktop** disables remote desktop access to a hosted service.</span></span>
<span data-ttu-id="00690-109">Du måste publicera tjänsten med cmdleten **Publishing-AzureServiceProject** när du har inaktiverat fjärråtkomst för att ändringarna ska börja gälla.</span><span class="sxs-lookup"><span data-stu-id="00690-109">You must publish the service using the **Publish-AzureServiceProject** cmdlet after disabling Remote Desktop access for the change to take effect.</span></span>

## <span data-ttu-id="00690-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="00690-110">EXAMPLES</span></span>

## <span data-ttu-id="00690-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="00690-111">PARAMETERS</span></span>

### <span data-ttu-id="00690-112">-PassThru</span><span class="sxs-lookup"><span data-stu-id="00690-112">-PassThru</span></span>
<span data-ttu-id="00690-113">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="00690-113">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="00690-114">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="00690-114">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00690-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="00690-115">-Profile</span></span>
<span data-ttu-id="00690-116">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="00690-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="00690-117">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="00690-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00690-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00690-118">CommonParameters</span></span>
<span data-ttu-id="00690-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00690-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00690-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00690-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00690-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="00690-121">INPUTS</span></span>

## <span data-ttu-id="00690-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="00690-122">OUTPUTS</span></span>

## <span data-ttu-id="00690-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="00690-123">NOTES</span></span>

## <span data-ttu-id="00690-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="00690-124">RELATED LINKS</span></span>

[<span data-ttu-id="00690-125">Enable-AzureServiceProjectRemoteDesktop</span><span class="sxs-lookup"><span data-stu-id="00690-125">Enable-AzureServiceProjectRemoteDesktop</span></span>](./Enable-AzureServiceProjectRemoteDesktop.md)


