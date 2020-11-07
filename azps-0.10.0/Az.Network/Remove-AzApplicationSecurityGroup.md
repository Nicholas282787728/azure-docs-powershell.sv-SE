---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationSecurityGroup.md
ms.openlocfilehash: 1bdad35adef15c15c77753c77533f35cfaf945ea
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922043"
---
# <span data-ttu-id="16c46-101">Remove-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="16c46-101">Remove-AzApplicationSecurityGroup</span></span>

## <span data-ttu-id="16c46-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="16c46-102">SYNOPSIS</span></span>
<span data-ttu-id="16c46-103">Tar bort en säkerhets grupp för program.</span><span class="sxs-lookup"><span data-stu-id="16c46-103">Removes an application security group.</span></span>

## <span data-ttu-id="16c46-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="16c46-104">SYNTAX</span></span>

```
Remove-AzApplicationSecurityGroup -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16c46-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="16c46-105">DESCRIPTION</span></span>
<span data-ttu-id="16c46-106">Cmdleten **Remove-AzApplicationSecurityGroup** tar bort en säkerhets grupp för program.</span><span class="sxs-lookup"><span data-stu-id="16c46-106">The **Remove-AzApplicationSecurityGroup** cmdlet removes an application security group.</span></span>

## <span data-ttu-id="16c46-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="16c46-107">EXAMPLES</span></span>

### <span data-ttu-id="16c46-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="16c46-108">Example 1</span></span>
```
PS C:\>Remove-AzApplicationSecurityGroup -Name "MyApplicationSecurityGrouo" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="16c46-109">Det här kommandot tar bort en säkerhets grupp för program med namnet MyApplicationSecurityGrouo i resurs gruppen med namnet MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="16c46-109">This command deletes an application security group named MyApplicationSecurityGrouo in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="16c46-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="16c46-110">PARAMETERS</span></span>

### <span data-ttu-id="16c46-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16c46-111">-DefaultProfile</span></span>
<span data-ttu-id="16c46-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="16c46-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="16c46-113">-Force</span><span class="sxs-lookup"><span data-stu-id="16c46-113">-Force</span></span>
<span data-ttu-id="16c46-114">Fråga inte efter bekräftelse om du vill ta bort resursen</span><span class="sxs-lookup"><span data-stu-id="16c46-114">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="16c46-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="16c46-115">-Name</span></span>
<span data-ttu-id="16c46-116">Namnet på program säkerhets gruppen.</span><span class="sxs-lookup"><span data-stu-id="16c46-116">The name of the application security group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16c46-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="16c46-117">-PassThru</span></span>
<span data-ttu-id="16c46-118">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="16c46-118">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="16c46-119">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="16c46-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="16c46-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16c46-120">-ResourceGroupName</span></span>
<span data-ttu-id="16c46-121">Resurs grupps namnet för program säkerhets gruppen.</span><span class="sxs-lookup"><span data-stu-id="16c46-121">The resource group name of the application security group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16c46-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="16c46-122">-Confirm</span></span>
<span data-ttu-id="16c46-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="16c46-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16c46-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16c46-124">-WhatIf</span></span>
<span data-ttu-id="16c46-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="16c46-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16c46-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="16c46-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16c46-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16c46-127">CommonParameters</span></span>
<span data-ttu-id="16c46-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16c46-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16c46-129">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16c46-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16c46-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="16c46-130">INPUTS</span></span>

### <span data-ttu-id="16c46-131">System. String</span><span class="sxs-lookup"><span data-stu-id="16c46-131">System.String</span></span>

## <span data-ttu-id="16c46-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="16c46-132">OUTPUTS</span></span>

### <span data-ttu-id="16c46-133">System. Object</span><span class="sxs-lookup"><span data-stu-id="16c46-133">System.Object</span></span>

## <span data-ttu-id="16c46-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="16c46-134">NOTES</span></span>

## <span data-ttu-id="16c46-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="16c46-135">RELATED LINKS</span></span>

[<span data-ttu-id="16c46-136">New-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="16c46-136">New-AzApplicationSecurityGroup</span></span>](./New-AzApplicationSecurityGroup.md)

[<span data-ttu-id="16c46-137">Get-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="16c46-137">Get-AzApplicationSecurityGroup</span></span>](./Get-AzApplicationSecurityGroup.md)
