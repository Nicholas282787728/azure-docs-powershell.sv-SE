---
title: Bevara autentiseringsuppgifter för användare mellan PowerShell-sessioner
description: Lär dig hur du återanvänder Azure-autentiseringsuppgifter och annan information över flera PowerShell-sessioner.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/09/2018
ms.openlocfilehash: 9867efc991f4a9efe880c0f449d9d2be1cddf8ef
ms.sourcegitcommit: bc88e64c494337821274d6a66c1edad656c119c5
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/20/2018
ms.locfileid: "46300637"
---
# <a name="persist-user-credentials-across-powershell-sessions"></a><span data-ttu-id="56d1b-103">Bevara autentiseringsuppgifter för användare mellan PowerShell-sessioner</span><span class="sxs-lookup"><span data-stu-id="56d1b-103">Persist user credentials across PowerShell sessions</span></span>

<span data-ttu-id="56d1b-104">Azure PowerShell erbjuder en funktion som kallas **Azure Context Autosave**, som ger följande funktioner:</span><span class="sxs-lookup"><span data-stu-id="56d1b-104">Azure PowerShell offers a feature called **Azure Context Autosave**, which gives the following features:</span></span>

- <span data-ttu-id="56d1b-105">Bevara inloggningsinformation för återanvändning i nya PowerShell-sessioner.</span><span class="sxs-lookup"><span data-stu-id="56d1b-105">Retention of sign-in information for reuse in new PowerShell sessions.</span></span>
- <span data-ttu-id="56d1b-106">Enklare användning av bakgrundsaktiviteter för att köra tidskrävande cmdletar.</span><span class="sxs-lookup"><span data-stu-id="56d1b-106">Easier use of background tasks for executing long-running cmdlets.</span></span>
- <span data-ttu-id="56d1b-107">Växla mellan konton, prenumerationer och miljöer utan separat inloggning.</span><span class="sxs-lookup"><span data-stu-id="56d1b-107">Switch between accounts, subscriptions, and environments without a separate sign-in.</span></span>
- <span data-ttu-id="56d1b-108">Köra uppgifter med olika autentiseringsuppgifter och prenumerationer, samtidigt från samma PowerShell-session.</span><span class="sxs-lookup"><span data-stu-id="56d1b-108">Execution of tasks using different credentials and subscriptions, simultaneously, from the same PowerShell session.</span></span>

## <a name="azure-contexts-defined"></a><span data-ttu-id="56d1b-109">Definitioner av Azure-kontexter</span><span class="sxs-lookup"><span data-stu-id="56d1b-109">Azure contexts defined</span></span>

<span data-ttu-id="56d1b-110">En *Azure-kontext* är en informationsuppsättning som definierar målet för Azure PowerShell-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="56d1b-110">An *Azure context* is a set of information that defines the target of Azure PowerShell cmdlets.</span></span> <span data-ttu-id="56d1b-111">Kontexten består av fem delar:</span><span class="sxs-lookup"><span data-stu-id="56d1b-111">The context consists of five parts:</span></span>

- <span data-ttu-id="56d1b-112">Ett *konto* – användarnamnet eller tjänstens huvudnamn som används för att autentisera kommunikationen med Azure</span><span class="sxs-lookup"><span data-stu-id="56d1b-112">An *Account* - the UserName or Service Principal used to authenticate communications with Azure</span></span>
- <span data-ttu-id="56d1b-113">En *prenumeration* – Azure-prenumerationen med de resurser där åtgärder vidtas.</span><span class="sxs-lookup"><span data-stu-id="56d1b-113">A *Subscription* - The Azure Subscription with the Resources being acted upon.</span></span>
- <span data-ttu-id="56d1b-114">En *klientorganisation* – Azure Active Directory-klienten som innehåller din prenumeration.</span><span class="sxs-lookup"><span data-stu-id="56d1b-114">A *Tenant* - The Azure Active Directory tenant that contains your subscription.</span></span> <span data-ttu-id="56d1b-115">Klienter är viktigare för ServicePrincipal-autentisering.</span><span class="sxs-lookup"><span data-stu-id="56d1b-115">Tenants are more important to ServicePrincipal authentication.</span></span>
- <span data-ttu-id="56d1b-116">En *miljö* – det specifika Azure-moln som är målet, vanligtvis det globala Azure-molnet.</span><span class="sxs-lookup"><span data-stu-id="56d1b-116">An *Environment* - The particular Azure Cloud being targeted, usually the Azure global Cloud.</span></span>
  <span data-ttu-id="56d1b-117">Med miljöinställningen kan du även ange nationella, offentliga och lokala moln (Azure Stack) som mål.</span><span class="sxs-lookup"><span data-stu-id="56d1b-117">However, the environment setting allows you to target National, Government, and on-premises (Azure Stack) clouds as well.</span></span>
- <span data-ttu-id="56d1b-118">*Autentiseringsuppgifter* – den information som används av Azure för att verifiera din identitet och bekräfta din behörighet att komma åt resurser i Azure</span><span class="sxs-lookup"><span data-stu-id="56d1b-118">*Credentials* - The information used by Azure to verify your identity and confirm your authorization to access resources in Azure</span></span>

<span data-ttu-id="56d1b-119">I tidigare versioner måste en Azure-kontext skapas varje gång du öppnade en ny PowerShell-session.</span><span class="sxs-lookup"><span data-stu-id="56d1b-119">In previous releases, an Azure Context had to be created each time you opened a new PowerShell session.</span></span> <span data-ttu-id="56d1b-120">Från och med Azure PowerShell v4.4.0 kan Azure-kontexter sparas automatiskt när du öppnar en ny PowerShell-session.</span><span class="sxs-lookup"><span data-stu-id="56d1b-120">Beginning with Azure PowerShell v4.4.0, Azure Contexts can automatically be saved whenever opening a new PowerShell session.</span></span>

## <a name="automatically-save-the-context-for-the-next-sign-in"></a><span data-ttu-id="56d1b-121">Spara automatiskt kontexten för nästa inloggning</span><span class="sxs-lookup"><span data-stu-id="56d1b-121">Automatically save the context for the next sign-in</span></span>

<span data-ttu-id="56d1b-122">I version 6.3.0 och senare behåller Azure PowerShell din kontextinformation mellan sessioner automatiskt.</span><span class="sxs-lookup"><span data-stu-id="56d1b-122">In versions 6.3.0 and later, Azure PowerShell retains your context information automatically between sessions.</span></span> <span data-ttu-id="56d1b-123">Om du vill ange att PowerShell ska glömma kontexten och autentiseringsuppgifterna ska du använda `Disable-AzureRmContextAutoSave`.</span><span class="sxs-lookup"><span data-stu-id="56d1b-123">To set PowerShell to forget your context and credentials, use `Disable-AzureRmContextAutoSave`.</span></span> <span data-ttu-id="56d1b-124">Du måste logga in på Azure varje gång du öppnar en PowerShell-session.</span><span class="sxs-lookup"><span data-stu-id="56d1b-124">You'll need to sign in to Azure every time you open a PowerShell session.</span></span>

<span data-ttu-id="56d1b-125">Om du vill tillåta Azure PowerShell att komma ihåg kontexten när PowerShell-sessionen avslutas ska du använda `Enable-AzureRmContextAutosave`.</span><span class="sxs-lookup"><span data-stu-id="56d1b-125">To allow Azure PowerShell to remember your context after the PowerShell session is closed, use `Enable-AzureRmContextAutosave`.</span></span> <span data-ttu-id="56d1b-126">Information om kontext och autentiseringsuppgifter sparas automatiskt i en särskild dold mapp i användarkatalogen (`%AppData%\Roaming\Windows Azure PowerShell`).</span><span class="sxs-lookup"><span data-stu-id="56d1b-126">Context and credential information are automatically saved in a special hidden folder in your user directory (`%AppData%\Roaming\Windows Azure PowerShell`).</span></span>
<span data-ttu-id="56d1b-127">I varje ny PowerShell-session används kontexten i den senaste sessionen som mål.</span><span class="sxs-lookup"><span data-stu-id="56d1b-127">Each new PowerShell session targets the context used in your last session.</span></span>

<span data-ttu-id="56d1b-128">Med de cmdletar du kan använda för att hantera Azure-kontexter kan du också göra mer detaljerade inställningar.</span><span class="sxs-lookup"><span data-stu-id="56d1b-128">The cmdlets that allow you to manage Azure contexts also allow you fine grained control.</span></span> <span data-ttu-id="56d1b-129">Om du vill att ändringarna ska tillämpas endast på den aktuella PowerShell-sessionen (omfånget `Process`) eller alla PowerShell-sessioner (omfånget `CurrentUser`).</span><span class="sxs-lookup"><span data-stu-id="56d1b-129">If you want changes to apply only to the current PowerShell session (`Process` scope) or every PowerShell session (`CurrentUser` scope).</span></span> <span data-ttu-id="56d1b-130">Dessa alternativ beskrivs mer detaljerat i [Använda kontextomfång](#Using-Context-Scopes).</span><span class="sxs-lookup"><span data-stu-id="56d1b-130">These options are discussed in mode detail in [Using Context Scopes](#Using-Context-Scopes).</span></span>

## <a name="running-azure-powershell-cmdlets-as-background-jobs"></a><span data-ttu-id="56d1b-131">Köra Azure PowerShell-cmdletar som bakgrundsjobb</span><span class="sxs-lookup"><span data-stu-id="56d1b-131">Running Azure PowerShell cmdlets as background jobs</span></span>

<span data-ttu-id="56d1b-132">Med funktionen **Azure Context Autosave** kan du också dela din kontext med PowerShell-bakgrundsjobb.</span><span class="sxs-lookup"><span data-stu-id="56d1b-132">The **Azure Context Autosave** feature also allows you to share you context with PowerShell background jobs.</span></span> <span data-ttu-id="56d1b-133">I PowerShell kan du starta och övervaka tidskrävande uppgifter som bakgrundsjobb utan att behöva vänta tills uppgifterna har slutförts.</span><span class="sxs-lookup"><span data-stu-id="56d1b-133">PowerShell allows you to start and monitor long-executing tasks as background jobs without having to wait for the tasks to complete.</span></span> <span data-ttu-id="56d1b-134">Du kan dela autentiseringsuppgifter med bakgrundsjobb på två olika sätt:</span><span class="sxs-lookup"><span data-stu-id="56d1b-134">You can share credentials with background jobs in two different ways:</span></span>

- <span data-ttu-id="56d1b-135">Skicka kontexten som ett argument</span><span class="sxs-lookup"><span data-stu-id="56d1b-135">Passing the context as an argument</span></span>

  <span data-ttu-id="56d1b-136">Med de flesta AzureRM-cmdletar kan du skicka kontexten som en parameter till cmdleten.</span><span class="sxs-lookup"><span data-stu-id="56d1b-136">Most AzureRM cmdlets allow you to pass the context as a parameter to the cmdlet.</span></span> <span data-ttu-id="56d1b-137">Du kan skicka en kontext till ett bakgrundsjobb enligt följande exempel:</span><span class="sxs-lookup"><span data-stu-id="56d1b-137">You can pass a context to a background job as shown in the following example:</span></span>

  ```powershell
  PS C:\> $job = Start-Job { param ($ctx) New-AzureRmVm -AzureRmContext $ctx [... Additional parameters ...]} -ArgumentList (Get-AzureRmContext)
  ```

- <span data-ttu-id="56d1b-138">Med hjälp av standardkontexten med spara automatiskt aktiverat</span><span class="sxs-lookup"><span data-stu-id="56d1b-138">Using the default context with Autosave enabled</span></span>

  <span data-ttu-id="56d1b-139">Om du har aktiverat **Context Autosave** (Spara automatiskt kontext) använder bakgrundsjobben automatiskt den sparade standardkontexten.</span><span class="sxs-lookup"><span data-stu-id="56d1b-139">If you have enabled **Context Autosave**, background jobs automatically use the default saved context.</span></span>

  ```powershell
  PS C:\> $job = Start-Job { New-AzureRmVm [... Additional parameters ...]}
  ```

<span data-ttu-id="56d1b-140">När du behöver veta resultatet av en bakgrundsaktivitet kan du använda `Get-Job` för att kontrollera jobbstatus och `Wait-Job` för att vänta tills jobbet är slutfört.</span><span class="sxs-lookup"><span data-stu-id="56d1b-140">When you need to know the outcome of the background task, use `Get-Job` to check the job status and `Wait-Job` to wait for the Job to complete.</span></span> <span data-ttu-id="56d1b-141">Använd `Receive-Job` för att registrera eller visa resultatet av bakgrundsjobbet.</span><span class="sxs-lookup"><span data-stu-id="56d1b-141">Use `Receive-Job` to capture or display the output of the background job.</span></span> <span data-ttu-id="56d1b-142">Mer information finns i artikeln [om jobb](/powershell/module/microsoft.powershell.core/about/about_jobs).</span><span class="sxs-lookup"><span data-stu-id="56d1b-142">For more information, see [about_Jobs](/powershell/module/microsoft.powershell.core/about/about_jobs).</span></span>

## <a name="creating-selecting-renaming-and-removing-contexts"></a><span data-ttu-id="56d1b-143">Skapa, välja, byta namn på och ta bort kontexter</span><span class="sxs-lookup"><span data-stu-id="56d1b-143">Creating, selecting, renaming, and removing contexts</span></span>

<span data-ttu-id="56d1b-144">Om du vill skapa en kontext måste du vara inloggad i Azure.</span><span class="sxs-lookup"><span data-stu-id="56d1b-144">To create a context, you must be signed in to Azure.</span></span> <span data-ttu-id="56d1b-145">Med cmdleten `Connect-AzureRmAccount` (eller dess alias `Login-AzureRmAccount`) anger du standardkontexten som används av Azure PowerShell-cmdletar och kan komma åt alla klienter eller prenumerationer som tillåts med dina autentiseringsuppgifter.</span><span class="sxs-lookup"><span data-stu-id="56d1b-145">The `Connect-AzureRmAccount` cmdlet (or its alias, `Login-AzureRmAccount`) sets the default context used by Azure PowerShell cmdlets, and allows you to access any tenants or subscriptions allowed by your credentials.</span></span>

<span data-ttu-id="56d1b-146">Om du vill lägga till en ny kontext efter inloggningen använder du `Set-AzureRmContext` (eller dess alias `Select-AzureRmSubscription`).</span><span class="sxs-lookup"><span data-stu-id="56d1b-146">To add a new context after sign-in, use `Set-AzureRmContext` (or its alias, `Select-AzureRmSubscription`).</span></span>

```azurepowershell-interactive
PS C:\> Set-AzureRMContext -Subscription "Contoso Subscription 1" -Name "Contoso1"
```

<span data-ttu-id="56d1b-147">I exemplet ovan läggs en ny kontext till med målet ”Contoso Subscription 1” med hjälp av dina aktuella autentiseringsuppgifter.</span><span class="sxs-lookup"><span data-stu-id="56d1b-147">The previous example adds a new context targeting 'Contoso Subscription 1' using your current credentials.</span></span> <span data-ttu-id="56d1b-148">Den nya kontexten har namnet ”Contoso1”.</span><span class="sxs-lookup"><span data-stu-id="56d1b-148">The new context is named 'Contoso1'.</span></span> <span data-ttu-id="56d1b-149">Om du inte anger ett namn för kontexten används ett standardnamn med konto-ID och prenumerations-ID.</span><span class="sxs-lookup"><span data-stu-id="56d1b-149">If you don't provide a name for the context, a default name, using the account ID and subscription ID is used.</span></span>

<span data-ttu-id="56d1b-150">Byt namn på en befintlig kontext genom att använda cmdlet `Rename-AzureRmContext`.</span><span class="sxs-lookup"><span data-stu-id="56d1b-150">To rename an existing context, use the `Rename-AzureRmContext` cmdlet.</span></span> <span data-ttu-id="56d1b-151">Exempel:</span><span class="sxs-lookup"><span data-stu-id="56d1b-151">For example:</span></span>

```azurepowershell-interactive
PS C:\> Rename-AzureRmContext '[user1@contoso.org; 123456-7890-1234-564321]` 'Contoso2'
```

<span data-ttu-id="56d1b-152">Det här exemplet byter namn på kontexten med det automatiska namnet `[user1@contoso.org; 123456-7890-1234-564321]` till ”Contoso2”.</span><span class="sxs-lookup"><span data-stu-id="56d1b-152">This example renames the context with automatic name `[user1@contoso.org; 123456-7890-1234-564321]` to the simple name 'Contoso2'.</span></span> <span data-ttu-id="56d1b-153">Cmdletar som hanterar kontexter använder också tabbifyllning, så att du snabbt kan välja kontexten.</span><span class="sxs-lookup"><span data-stu-id="56d1b-153">Cmdlets that manage contexts also use tab completion, allowing you to quickly select the context.</span></span>

<span data-ttu-id="56d1b-154">Slutligen, för att ta bort en kontext använder du cmdlet `Remove-AzureRmContext`.</span><span class="sxs-lookup"><span data-stu-id="56d1b-154">Finally, to remove a context, use the `Remove-AzureRmContext` cmdlet.</span></span>  <span data-ttu-id="56d1b-155">Exempel:</span><span class="sxs-lookup"><span data-stu-id="56d1b-155">For example:</span></span>

```azurepowershell-interactive
PS C:\> Remove-AzureRmContext Contoso2
```

<span data-ttu-id="56d1b-156">Glömmer kontexten med namnet ”Contoso2”.</span><span class="sxs-lookup"><span data-stu-id="56d1b-156">Forgets the context that was named 'Contoso2'.</span></span> <span data-ttu-id="56d1b-157">Du kan återskapa den här kontexten med hjälp av `Set-AzureRmContext`</span><span class="sxs-lookup"><span data-stu-id="56d1b-157">You can recreate this context using `Set-AzureRmContext`</span></span>

## <a name="removing-credentials"></a><span data-ttu-id="56d1b-158">Ta bort autentiseringsuppgifter</span><span class="sxs-lookup"><span data-stu-id="56d1b-158">Removing credentials</span></span>

<span data-ttu-id="56d1b-159">Du kan ta bort alla autentiseringsuppgifter och associerade kontexter för en användare eller en tjänsts huvudnamn med hjälp av `Disconnect-AzureRmAccount` (kallas även `Logout-AzureRmAccount`).</span><span class="sxs-lookup"><span data-stu-id="56d1b-159">You can remove all credentials and associated contexts for a user or service principal using `Disconnect-AzureRmAccount` (also known as `Logout-AzureRmAccount`).</span></span> <span data-ttu-id="56d1b-160">När den körs utan parametrar tar cmdleten `Disconnect-AzureRmAccount` bort alla autentiseringsuppgifter och kontexter som är associerade med användaren eller tjänstens huvudnamn i den aktuella kontexten.</span><span class="sxs-lookup"><span data-stu-id="56d1b-160">When executed without parameters, the `Disconnect-AzureRmAccount` cmdlet removes all credentials and contexts associated with the User or Service Principal in the current context.</span></span> <span data-ttu-id="56d1b-161">Du kan skicka användarnamn, tjänstens huvudnamn eller kontext med ett visst huvudkonto som mål.</span><span class="sxs-lookup"><span data-stu-id="56d1b-161">You may pass in a Username, Service Principal Name, or context to target a particular principal.</span></span>

```azurepowershell-interactive
Disconnect-AzureRmAccount user1@contoso.org
```

## <a name="using-context-scopes"></a><span data-ttu-id="56d1b-162">Använda kontextomfång</span><span class="sxs-lookup"><span data-stu-id="56d1b-162">Using context scopes</span></span>

<span data-ttu-id="56d1b-163">Ibland kan vilja du markera, ändra eller ta bort en kontext i en PowerShell-session utan att påverka andra sessioner.</span><span class="sxs-lookup"><span data-stu-id="56d1b-163">Occasionally, you may want to select, change, or remove a context in a PowerShell session without impacting other sessions.</span></span> <span data-ttu-id="56d1b-164">Om du vill ändra standardbeteendet för kontext-cmdletar ska du använda parametern `Scope`.</span><span class="sxs-lookup"><span data-stu-id="56d1b-164">To change the default behavior of context cmdlets, use the `Scope` parameter.</span></span> <span data-ttu-id="56d1b-165">Omfånget `Process` åsidosätter standardbeteendet genom att tillämpa det endast i den aktuella sessionen.</span><span class="sxs-lookup"><span data-stu-id="56d1b-165">The `Process` scope overrides the default behavior by making it apply only for the current session.</span></span> <span data-ttu-id="56d1b-166">Däremot ändrar omfånget `CurrentUser` kontexten i alla sessioner, inte bara i den aktuella sessionen.</span><span class="sxs-lookup"><span data-stu-id="56d1b-166">Conversely `CurrentUser` scope changes the context in all sessions, instead of just the current session.</span></span>

<span data-ttu-id="56d1b-167">Om du till exempel vill ändra standardkontexten i den aktuella PowerShell-sessionen utan att påverka andra fönster eller den kontext som används nästa gång en session öppnas, ska du använda:</span><span class="sxs-lookup"><span data-stu-id="56d1b-167">As an example, to change the default context in the current PowerShell session without impacting other windows, or the context used the next time a session is opened, use:</span></span>

```azurepowershell-interactive
PS C:\> Select-AzureRmContext Contoso1 -Scope Process
```

## <a name="how-the-context-autosave-setting-is-remembered"></a><span data-ttu-id="56d1b-168">Hur inställningen spara automatiskt kontext bevaras</span><span class="sxs-lookup"><span data-stu-id="56d1b-168">How the context autosave setting is remembered</span></span>

<span data-ttu-id="56d1b-169">Inställningen för att spara kontext automatiskt sparas i användarens Azure PowerShell-katalog (`%AppData%\Roaming\Windows Azure PowerShell`).</span><span class="sxs-lookup"><span data-stu-id="56d1b-169">The context AutoSave setting is saved to the user Azure PowerShell directory (`%AppData%\Roaming\Windows Azure PowerShell`).</span></span> <span data-ttu-id="56d1b-170">Vissa typer av datorkonton kanske inte har åtkomst till den här katalogen.</span><span class="sxs-lookup"><span data-stu-id="56d1b-170">Some kinds of computer accounts may not have access to this directory.</span></span> <span data-ttu-id="56d1b-171">I sådana scenarier kan du använda miljövariabeln</span><span class="sxs-lookup"><span data-stu-id="56d1b-171">For such scenarios, you can use the environment variable</span></span>

```azurepowershell-interactive
$env:AzureRmContextAutoSave="true" | "false"
```

<span data-ttu-id="56d1b-172">När värdet är true sparas kontexten automatiskt.</span><span class="sxs-lookup"><span data-stu-id="56d1b-172">When set to 'true', the context is automatically saved.</span></span> <span data-ttu-id="56d1b-173">Om värdet är false sparas inte kontexten.</span><span class="sxs-lookup"><span data-stu-id="56d1b-173">If set to 'false', the context isn't saved.</span></span>

## <a name="changes-to-the-azurermprofile-module"></a><span data-ttu-id="56d1b-174">Ändringar i modulen AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="56d1b-174">Changes to the AzureRM.Profile module</span></span>

<span data-ttu-id="56d1b-175">Nya cmdletar för att hantera kontext</span><span class="sxs-lookup"><span data-stu-id="56d1b-175">New cmdlets for managing context</span></span>

- <span data-ttu-id="56d1b-176">[Enable-AzureRmContextAutosave][enable] – Tillåt att kontexten sparas mellan PowerShell-sessioner.</span><span class="sxs-lookup"><span data-stu-id="56d1b-176">[Enable-AzureRmContextAutosave][enable] - Allow saving the context between powershell sessions.</span></span>
  <span data-ttu-id="56d1b-177">Eventuella ändringar ändrar den globala kontexten.</span><span class="sxs-lookup"><span data-stu-id="56d1b-177">Any changes alter the global context.</span></span>
- <span data-ttu-id="56d1b-178">[Disable-AzureRmContextAutosave][disable] – Inaktivera automatiskt sparande av kontexten.</span><span class="sxs-lookup"><span data-stu-id="56d1b-178">[Disable-AzureRmContextAutosave][disable] - Turn off autosaving the context.</span></span> <span data-ttu-id="56d1b-179">Inloggning krävs för varje ny PowerShell-session.</span><span class="sxs-lookup"><span data-stu-id="56d1b-179">Each new PowerShell session is required to sign in again.</span></span>
- <span data-ttu-id="56d1b-180">[Select-AzureRmContext][select] – Välj en kontext som standard.</span><span class="sxs-lookup"><span data-stu-id="56d1b-180">[Select-AzureRmContext][select] - Select a context as the default.</span></span> <span data-ttu-id="56d1b-181">Alla cmdletar använder autentiseringsuppgifterna i den här kontexten för autentisering.</span><span class="sxs-lookup"><span data-stu-id="56d1b-181">All cmdlets use the credentials in this context for authentication.</span></span>
- <span data-ttu-id="56d1b-182">[Disconnect-AzureRmAccount][remove-cred] – Ta bort alla autentiseringsuppgifter och kontexter som är kopplade till ett konto.</span><span class="sxs-lookup"><span data-stu-id="56d1b-182">[Disconnect-AzureRmAccount][remove-cred] - Remove all credentials and contexts associated with an account.</span></span>
- <span data-ttu-id="56d1b-183">[Remove-AzureRmContext][remove-context] – Ta bort en namngiven kontext.</span><span class="sxs-lookup"><span data-stu-id="56d1b-183">[Remove-AzureRmContext][remove-context] - Remove a named context.</span></span>
- <span data-ttu-id="56d1b-184">[Rename-AzureRmContext][rename] – Byt namn på en befintlig kontext.</span><span class="sxs-lookup"><span data-stu-id="56d1b-184">[Rename-AzureRmContext][rename] - Rename an existing context.</span></span>

<span data-ttu-id="56d1b-185">Ändringar av befintliga profil-cmdletar</span><span class="sxs-lookup"><span data-stu-id="56d1b-185">Changes to existing profile cmdlets</span></span>

- <span data-ttu-id="56d1b-186">[Add-AzureRmAccount][login] – Gör det möjligt att ange omfång för inloggningen till processen eller till den aktuella användaren.</span><span class="sxs-lookup"><span data-stu-id="56d1b-186">[Add-AzureRmAccount][login] - Allow scoping of the sign-in to the process or the current user.</span></span>
  <span data-ttu-id="56d1b-187">Gör det möjligt att ge standardkontexten ett namn efter autentisering.</span><span class="sxs-lookup"><span data-stu-id="56d1b-187">Allow naming the default context after authentication.</span></span>
- <span data-ttu-id="56d1b-188">[Import-AzureRmContext][import] – Gör det möjligt att ange omfång för inloggningen till processen eller till den aktuella användaren.</span><span class="sxs-lookup"><span data-stu-id="56d1b-188">[Import-AzureRmContext][import] - Allow scoping of the sign-in to the process or the current user.</span></span>
- <span data-ttu-id="56d1b-189">[Set-AzureRmContext][set-context] – Gör det möjligt att välja befintliga, namngivna kontexter och ändra omfång till processen eller till den aktuella användaren.</span><span class="sxs-lookup"><span data-stu-id="56d1b-189">[Set-AzureRmContext][set-context] - Allow selection of existing named contexts, and scope changes to the process or current user.</span></span>

<!-- Hyperlinks -->
[enable]: /powershell/module/azurerm.profile/Enable-AzureRmContextAutosave
[disable]: /powershell/module/azurerm.profile/Disable-AzureRmContextAutosave
[select]: /powershell/module/azurerm.profile/Select-AzureRmContext
[remove-cred]: /powershell/module/azurerm.profile/Disconnect-AzureRmAccount
[remove-context]: /powershell/module/azurerm.profile/Remove-AzureRmContext
[rename]: /powershell/module/azurerm.profile/Rename-AzureRmContext

<!-- Updated cmdlets -->
[login]: /powershell/module/azurerm.profile/Connect-AzureRmAccount
[import]:  /powershell/module/azurerm.profile/Import-AzureRmContext
[set-context]: /powershell/module/azurerm.profile/Set-AzureRmContext
