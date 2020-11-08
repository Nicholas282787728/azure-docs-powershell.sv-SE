---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 163D2F00-E041-43A9-B077-9034F54B4F3D
online version: ''
schema: 2.0.0
ms.openlocfilehash: cf258a8f13a344b09f9d5c7119cd78ad202d2ca0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093409"
---
# <span data-ttu-id="0cab0-101">Enable-AzureServiceProjectRemoteDesktop</span><span class="sxs-lookup"><span data-stu-id="0cab0-101">Enable-AzureServiceProjectRemoteDesktop</span></span>

## <span data-ttu-id="0cab0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0cab0-102">SYNOPSIS</span></span>
<span data-ttu-id="0cab0-103">Möjliggör åtkomst till fjärr skrivbord till en moln tjänst.</span><span class="sxs-lookup"><span data-stu-id="0cab0-103">Enables remote desktop access to a cloud service.</span></span>

## <span data-ttu-id="0cab0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0cab0-104">SYNTAX</span></span>

```
Enable-AzureServiceProjectRemoteDesktop -Username <String> -Password <SecureString> [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="0cab0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0cab0-105">DESCRIPTION</span></span>
<span data-ttu-id="0cab0-106">I det här avsnittet beskrivs cmdleten i 0.8.10-versionen av Microsoft Azure PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="0cab0-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="0cab0-107">För att få den version av modulen du använder, gå till Azure PowerShell-konsolen och skriv `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="0cab0-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="0cab0-108">Cmdleten **Enable-AzureServiceProjectRemoteDesktop** möjliggör åtkomst till fjärr skrivbord till en moln tjänst.</span><span class="sxs-lookup"><span data-stu-id="0cab0-108">The **Enable-AzureServiceProjectRemoteDesktop** cmdlet enables Remote Desktop access to a cloud service.</span></span>
<span data-ttu-id="0cab0-109">Du måste publicera tjänsten med cmdleten **Publishing-AzureServiceProject** när du har aktiverat funktionen för att ändringarna ska börja gälla.</span><span class="sxs-lookup"><span data-stu-id="0cab0-109">You must publish the service using the **Publish-AzureServiceProject** cmdlet after enabling Remote Desktop access for the change to take effect.</span></span>

## <span data-ttu-id="0cab0-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0cab0-110">EXAMPLES</span></span>

## <span data-ttu-id="0cab0-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0cab0-111">PARAMETERS</span></span>

### <span data-ttu-id="0cab0-112">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0cab0-112">-PassThru</span></span>
<span data-ttu-id="0cab0-113">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="0cab0-113">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0cab0-114">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="0cab0-114">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0cab0-115">-Lösen ord</span><span class="sxs-lookup"><span data-stu-id="0cab0-115">-Password</span></span>
<span data-ttu-id="0cab0-116">Anger lösen ordet.</span><span class="sxs-lookup"><span data-stu-id="0cab0-116">Specifies the password.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: pwd

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cab0-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="0cab0-117">-Profile</span></span>
<span data-ttu-id="0cab0-118">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="0cab0-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0cab0-119">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="0cab0-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0cab0-120">-Username</span><span class="sxs-lookup"><span data-stu-id="0cab0-120">-Username</span></span>
<span data-ttu-id="0cab0-121">Anger det användar namn som ska användas när du ansluter till roll instansen i Azure via Remote Desktop Protocol (RDP).</span><span class="sxs-lookup"><span data-stu-id="0cab0-121">Specifies the user name to use when connecting to the role instance in Azure via the Remote Desktop Protocol (RDP).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: user

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cab0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cab0-122">CommonParameters</span></span>
<span data-ttu-id="0cab0-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0cab0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cab0-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0cab0-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cab0-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0cab0-125">INPUTS</span></span>

## <span data-ttu-id="0cab0-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0cab0-126">OUTPUTS</span></span>

## <span data-ttu-id="0cab0-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0cab0-127">NOTES</span></span>

## <span data-ttu-id="0cab0-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0cab0-128">RELATED LINKS</span></span>

[<span data-ttu-id="0cab0-129">Disable-AzureServiceProjectRemoteDesktop</span><span class="sxs-lookup"><span data-stu-id="0cab0-129">Disable-AzureServiceProjectRemoteDesktop</span></span>](./Disable-AzureServiceProjectRemoteDesktop.md)

[<span data-ttu-id="0cab0-130">Publicera – AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="0cab0-130">Publish-AzureServiceProject</span></span>](./Publish-AzureServiceProject.md)


