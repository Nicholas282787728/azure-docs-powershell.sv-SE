---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 3FBF91B8-8EF9-4E05-AD7E-AEFC6EBBFB8E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceLock.md
ms.openlocfilehash: 2dbbb41ce1ad2ee6fc2279e711722090f4f1a6cc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98398123"
---
# <span data-ttu-id="770fd-101">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="770fd-101">Get-AzResourceLock</span></span>

## <span data-ttu-id="770fd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="770fd-102">SYNOPSIS</span></span>
<span data-ttu-id="770fd-103">Får ett resurs lås.</span><span class="sxs-lookup"><span data-stu-id="770fd-103">Gets a resource lock.</span></span>

## <span data-ttu-id="770fd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="770fd-104">SYNTAX</span></span>

### <span data-ttu-id="770fd-105">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="770fd-105">ByResourceGroup</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="770fd-106">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="770fd-106">ByResourceGroupLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="770fd-107">BySpecifiedScope</span><span class="sxs-lookup"><span data-stu-id="770fd-107">BySpecifiedScope</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="770fd-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="770fd-108">BySubscription</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="770fd-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="770fd-109">BySubscriptionLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="770fd-110">ByLockId</span><span class="sxs-lookup"><span data-stu-id="770fd-110">ByLockId</span></span>
```
Get-AzResourceLock [-AtScope] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="770fd-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="770fd-111">DESCRIPTION</span></span>
<span data-ttu-id="770fd-112">Cmdleten **Get-AzResourceLock** får Azure Resource lock.</span><span class="sxs-lookup"><span data-stu-id="770fd-112">The **Get-AzResourceLock** cmdlet gets Azure resource locks.</span></span>

## <span data-ttu-id="770fd-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="770fd-113">EXAMPLES</span></span>

### <span data-ttu-id="770fd-114">Exempel 1: skaffa ett lås</span><span class="sxs-lookup"><span data-stu-id="770fd-114">Example 1: Get a lock</span></span>
```
PS C:\>Get-AzResourceLock -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="770fd-115">Det här kommandot får resurs låset med namnet ContosoSiteLock.</span><span class="sxs-lookup"><span data-stu-id="770fd-115">This command gets the resource lock named ContosoSiteLock.</span></span>

### <span data-ttu-id="770fd-116">Exempel 2: Hämta lås på resurs grupps nivå eller högre</span><span class="sxs-lookup"><span data-stu-id="770fd-116">Example 2: Get locks at resource group level or higher</span></span>
```
PS C:\> Get-AzResourceLock -ResourceGroupName "ResourceGroup11" -AtScope
```

<span data-ttu-id="770fd-117">Det här kommandot får resursens lås för resurs gruppen eller prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="770fd-117">This command gets the resource locks on the resource group or the subscription.</span></span>

## <span data-ttu-id="770fd-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="770fd-118">PARAMETERS</span></span>

### <span data-ttu-id="770fd-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="770fd-119">-ApiVersion</span></span>
<span data-ttu-id="770fd-120">Anger vilken version av API för Resource provider som ska användas.</span><span class="sxs-lookup"><span data-stu-id="770fd-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="770fd-121">Om du inte anger en version använder denna cmdlet den senaste tillgängliga versionen.</span><span class="sxs-lookup"><span data-stu-id="770fd-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="770fd-122">-AtScope</span><span class="sxs-lookup"><span data-stu-id="770fd-122">-AtScope</span></span>
<span data-ttu-id="770fd-123">Anger att denna cmdlet returnerar alla lås på eller ovanför det angivna omfånget.</span><span class="sxs-lookup"><span data-stu-id="770fd-123">Indicates that this cmdlet returns all locks at or above the specified scope.</span></span>
<span data-ttu-id="770fd-124">Om du inte anger den här parametern returnerar cmdleten alla lås på, ovanför eller under scopet.</span><span class="sxs-lookup"><span data-stu-id="770fd-124">If you do not specify this parameter, the cmdlet returns all locks at, above, or below the scope.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="770fd-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="770fd-125">-DefaultProfile</span></span>
<span data-ttu-id="770fd-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="770fd-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="770fd-127">-LockId</span><span class="sxs-lookup"><span data-stu-id="770fd-127">-LockId</span></span>
<span data-ttu-id="770fd-128">Anger ID för det lås som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="770fd-128">Specifies the ID of the lock that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByLockId
Aliases: Id, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="770fd-129">-LockName</span><span class="sxs-lookup"><span data-stu-id="770fd-129">-LockName</span></span>
<span data-ttu-id="770fd-130">Anger namnet på det lås som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="770fd-130">Specifies the name of the lock that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup, ByResourceGroupLevel, BySpecifiedScope, BySubscription, BySubscriptionLevel
Aliases: ExtensionResourceName, Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="770fd-131">-För</span><span class="sxs-lookup"><span data-stu-id="770fd-131">-Pre</span></span>
<span data-ttu-id="770fd-132">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="770fd-132">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="770fd-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="770fd-133">-ResourceGroupName</span></span>
<span data-ttu-id="770fd-134">Anger namnet på den resurs grupp som låset gäller för.</span><span class="sxs-lookup"><span data-stu-id="770fd-134">Specifies the name of the resource group for which the lock applies.</span></span>
<span data-ttu-id="770fd-135">Denna cmdlet hämtar lås för den här resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="770fd-135">This cmdlet gets locks for this resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup, ByResourceGroupLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="770fd-136">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="770fd-136">-ResourceName</span></span>
<span data-ttu-id="770fd-137">Anger namnet på resursen som låset gäller för.</span><span class="sxs-lookup"><span data-stu-id="770fd-137">Specifies the name of the resource for which this lock applies.</span></span>
<span data-ttu-id="770fd-138">Denna cmdlet hämtar lås för den här resursen.</span><span class="sxs-lookup"><span data-stu-id="770fd-138">This cmdlet gets locks for this resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="770fd-139">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="770fd-139">-ResourceType</span></span>
<span data-ttu-id="770fd-140">Anger resurs typen för den resurs som den här låset gäller för.</span><span class="sxs-lookup"><span data-stu-id="770fd-140">Specifies the resource type of the resource for which this lock applies.</span></span>
<span data-ttu-id="770fd-141">Denna cmdlet hämtar lås för den här resursen.</span><span class="sxs-lookup"><span data-stu-id="770fd-141">This cmdlet gets locks for this resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="770fd-142">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="770fd-142">-Scope</span></span>
<span data-ttu-id="770fd-143">Anger omfattningen som låset gäller för.</span><span class="sxs-lookup"><span data-stu-id="770fd-143">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="770fd-144">Cmdleten får lås för detta scope.</span><span class="sxs-lookup"><span data-stu-id="770fd-144">The cmdlet gets locks for this scope.</span></span>

```yaml
Type: System.String
Parameter Sets: BySpecifiedScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="770fd-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="770fd-145">CommonParameters</span></span>
<span data-ttu-id="770fd-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="770fd-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="770fd-147">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="770fd-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="770fd-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="770fd-148">INPUTS</span></span>

### <span data-ttu-id="770fd-149">System. String</span><span class="sxs-lookup"><span data-stu-id="770fd-149">System.String</span></span>

## <span data-ttu-id="770fd-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="770fd-150">OUTPUTS</span></span>

### <span data-ttu-id="770fd-151">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="770fd-151">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="770fd-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="770fd-152">NOTES</span></span>

## <span data-ttu-id="770fd-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="770fd-153">RELATED LINKS</span></span>

[<span data-ttu-id="770fd-154">New-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="770fd-154">New-AzResourceLock</span></span>](./New-AzResourceLock.md)

[<span data-ttu-id="770fd-155">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="770fd-155">Remove-AzResourceLock</span></span>](./Remove-AzResourceLock.md)

[<span data-ttu-id="770fd-156">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="770fd-156">Set-AzResourceLock</span></span>](./Set-AzResourceLock.md)


