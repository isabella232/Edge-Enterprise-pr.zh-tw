---
title: 規則運算式 2 語法
ms.author: comanea
author: dan-wesley
manager: seanlyn
ms.date: 06/09/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: 規則運算式 2 語法
ms.openlocfilehash: 9654a25d2c0474601fb719b145ebb1f59241a6d9
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/31/2020
ms.locfileid: "10979518"
---
# <span data-ttu-id="9e66a-103">規則運算式 2 (re2.h) 語法</span><span class="sxs-lookup"><span data-stu-id="9e66a-103">Regular Expression 2 (re2.h) syntax</span></span>

<span data-ttu-id="9e66a-104">規則運算式是描述字元字串集的標記法。</span><span class="sxs-lookup"><span data-stu-id="9e66a-104">Regular expressions are a notation for describing sets of character strings.</span></span> <span data-ttu-id="9e66a-105">如果字串位於規則運算式所描述的集中，我們通常表示規則運算式與字串相符。</span><span class="sxs-lookup"><span data-stu-id="9e66a-105">When a string is in the set described by a regular expression, we often say that the regular expression matches the string.</span></span>

<span data-ttu-id="9e66a-106">最簡單的規則運算式是單一常值字元。</span><span class="sxs-lookup"><span data-stu-id="9e66a-106">The simplest regular expression is a single literal character.</span></span> <span data-ttu-id="9e66a-107">除*\*+?()|* 以外的元字元，字元與其本身相符。</span><span class="sxs-lookup"><span data-stu-id="9e66a-107">Except for the metacharacters like *\*+?()|*, characters match themselves.</span></span> <span data-ttu-id="9e66a-108">若要與元字元相符，請以反斜線將它轉義：\+ 符合常值加字元。</span><span class="sxs-lookup"><span data-stu-id="9e66a-108">To match a metacharacter, escape it with a backslash: \+ matches a literal plus character.</span></span>

<span data-ttu-id="9e66a-109">可以變更或串連兩個規則運算式，以形成新規則運算式：如果 *e<sub>1</sub>* 符合 _s_ 和*e<sub>2</sub>* 符合 _t_，則*<sub>1</sub>*  | *e<sub>2</sub> *符合 _s_ 或 _t_，以及*e<sub>1</sub>* *e<sub>2</sub>* 符合__ st。</span><span class="sxs-lookup"><span data-stu-id="9e66a-109">Two regular expressions can be altered or concatenated to form a new regular expression: if *e<sub>1</sub>* matches _s_ and *e<sub>2</sub>* matches _t_, then *e<sub>1</sub>* | *e<sub>2</sub>* matches _s_ or _t_, and *e<sub>1</sub>* *e<sub>2</sub>*  matches _st_.</span></span>

<span data-ttu-id="9e66a-110">元字元_\*_、_+_，以及 _？_</span><span class="sxs-lookup"><span data-stu-id="9e66a-110">The metacharacters _\*_ , _+_ , and _?_</span></span> <span data-ttu-id="9e66a-111">是重複運算子：*e<sub>1</sub>* _\*_ 與零個或多個 (可能不同的) 字串順序相符，其中每個字串都符合 *e<sub>1</sub>*；*e<sub>1</sub>* _+_ 符合一或多個；*e<sub>1</sub>* _？_</span><span class="sxs-lookup"><span data-stu-id="9e66a-111">are repetition operators: *e<sub>1</sub>* _\*_ matches a sequence of zero or more (possibly different) strings, each of which match *e<sub>1</sub>*; *e<sub>1</sub>* _+_ matches one or more; *e<sub>1</sub>* _?_</span></span> <span data-ttu-id="9e66a-112">符合零或一。</span><span class="sxs-lookup"><span data-stu-id="9e66a-112">matches zero or one.</span></span>

<span data-ttu-id="9e66a-113">運算子的優先順序 (從最弱到最强的繫結)，首先是替代，然後是串連，最後是重複運算子。</span><span class="sxs-lookup"><span data-stu-id="9e66a-113">The operator precedence, from weakest to strongest binding, is first alternation, then concatenation, and finally the repetition operators.</span></span> <span data-ttu-id="9e66a-114">顯式括弧可以用於強制不同的意義，就像在算術運算式中一樣。</span><span class="sxs-lookup"><span data-stu-id="9e66a-114">Explicit parentheses can be used to force different meanings, just as in arithmetic expressions.</span></span> <span data-ttu-id="9e66a-115">一些範例：_ab|cd_ 等同于_ (ab)|(cd)_ ； _ab\*_ 等同于 _a(b\*)_ 。</span><span class="sxs-lookup"><span data-stu-id="9e66a-115">Some examples: _ab|cd_ is equivalent to _(ab)|(cd)_ ; _ab\*_ is equivalent to _a(b\*)_ .</span></span>

<span data-ttu-id="9e66a-116">到目前為止描述的語法是大多數傳統的 Unix _egrep_ 規則運算式語法。</span><span class="sxs-lookup"><span data-stu-id="9e66a-116">The syntax described so far is most of the traditional Unix _egrep_ regular expression syntax.</span></span> <span data-ttu-id="9e66a-117">這個子集足以描述所有的常規語言：不嚴格地說，規則語言是一組字串，這些字串只需使用固定的記憶體量就可以在一次通過文字時進行匹配。</span><span class="sxs-lookup"><span data-stu-id="9e66a-117">This subset suffices to describe all regular languages: loosely speaking, a regular language is a set of strings that can be matched in a single pass through the text using only a fixed amount of memory.</span></span> <span data-ttu-id="9e66a-118">較新的規則運算式設備 (特別是 Perl 和那些複製它的設備) 新增了許多新的運算子和逸出序列，這使得規則運算式更簡潔，有時更神秘，但通常不是更强大。</span><span class="sxs-lookup"><span data-stu-id="9e66a-118">Newer regular expression facilities (notably Perl and those that have copied it) have added many new operators and escape sequences, which make the regular expressions more concise, and sometimes more cryptic, but usually not more powerful.</span></span>

<span data-ttu-id="9e66a-119">此頁面列出了 RE2 接受的規則運算式語法。</span><span class="sxs-lookup"><span data-stu-id="9e66a-119">This page lists the regular expression syntax accepted by RE2.</span></span>

<span data-ttu-id="9e66a-120">它也列出了一些 PCRE、PERL 和 VIM 接受的語法。</span><span class="sxs-lookup"><span data-stu-id="9e66a-120">It also lists some syntax accepted by PCRE, PERL and VIM.</span></span>

## <span data-ttu-id="9e66a-121">語法資料表</span><span class="sxs-lookup"><span data-stu-id="9e66a-121">Syntax tables</span></span>

| <span data-ttu-id="9e66a-122">各種單字元運算式</span><span class="sxs-lookup"><span data-stu-id="9e66a-122">Kinds of single-character expressions</span></span> | <span data-ttu-id="9e66a-123">範例</span><span class="sxs-lookup"><span data-stu-id="9e66a-123">Examples</span></span> |
| --- | --- |
| <span data-ttu-id="9e66a-124">任何字元，可能包括新行字元 (s=true)</span><span class="sxs-lookup"><span data-stu-id="9e66a-124">any character, possibly including newline (s=true)</span></span> | <span data-ttu-id="9e66a-125">.</span><span class="sxs-lookup"><span data-stu-id="9e66a-125">.</span></span> |
| <span data-ttu-id="9e66a-126">字元類別</span><span class="sxs-lookup"><span data-stu-id="9e66a-126">character class</span></span> | <span data-ttu-id="9e66a-127">[xyz]</span><span class="sxs-lookup"><span data-stu-id="9e66a-127">[xyz]</span></span> |
| <span data-ttu-id="9e66a-128">反字元類別</span><span class="sxs-lookup"><span data-stu-id="9e66a-128">negated character class</span></span> | <span data-ttu-id="9e66a-129">[^xyz]</span><span class="sxs-lookup"><span data-stu-id="9e66a-129">[^xyz]</span></span> |
| <span data-ttu-id="9e66a-130">Perl 字元類別 ([連結](#user-content-perl))</span><span class="sxs-lookup"><span data-stu-id="9e66a-130">Perl character class ([link](#user-content-perl))</span></span> | <span data-ttu-id="9e66a-131">\d</span><span class="sxs-lookup"><span data-stu-id="9e66a-131">\d</span></span> |
| <span data-ttu-id="9e66a-132">反 Perl 字元類別</span><span class="sxs-lookup"><span data-stu-id="9e66a-132">negated Perl character class</span></span> | <span data-ttu-id="9e66a-133">\D</span><span class="sxs-lookup"><span data-stu-id="9e66a-133">\D</span></span> |
| <span data-ttu-id="9e66a-134">ASCII 字元類別 ([連結](#user-content-ascii))</span><span class="sxs-lookup"><span data-stu-id="9e66a-134">ASCII character class ([link](#user-content-ascii))</span></span> | <span data-ttu-id="9e66a-135">[[:alpha:]]</span><span class="sxs-lookup"><span data-stu-id="9e66a-135">[[:alpha:]]</span></span> |
| <span data-ttu-id="9e66a-136">反 ASCII 字元類別</span><span class="sxs-lookup"><span data-stu-id="9e66a-136">negated ASCII character class</span></span> | <span data-ttu-id="9e66a-137">[[:^alpha:]]</span><span class="sxs-lookup"><span data-stu-id="9e66a-137">[[:^alpha:]]</span></span> |
| <span data-ttu-id="9e66a-138">Unicode 字元類別 (單字母名稱)</span><span class="sxs-lookup"><span data-stu-id="9e66a-138">Unicode character class (one-letter name)</span></span> | <span data-ttu-id="9e66a-139">\pN</span><span class="sxs-lookup"><span data-stu-id="9e66a-139">\pN</span></span> |
| <span data-ttu-id="9e66a-140">Unicode 字元類別</span><span class="sxs-lookup"><span data-stu-id="9e66a-140">Unicode character class</span></span> | <span data-ttu-id="9e66a-141">\p{Greek}</span><span class="sxs-lookup"><span data-stu-id="9e66a-141">\p{Greek}</span></span> |
| <span data-ttu-id="9e66a-142">反 Unicode 字元類 (單字母名稱)</span><span class="sxs-lookup"><span data-stu-id="9e66a-142">negated Unicode character class (one-letter name)</span></span> | <span data-ttu-id="9e66a-143">\PN</span><span class="sxs-lookup"><span data-stu-id="9e66a-143">\PN</span></span> |
| <span data-ttu-id="9e66a-144">反 Unicode 字元類別</span><span class="sxs-lookup"><span data-stu-id="9e66a-144">negated Unicode character class</span></span> | <span data-ttu-id="9e66a-145">\P{Greek}</span><span class="sxs-lookup"><span data-stu-id="9e66a-145">\P{Greek}</span></span> |

| | <span data-ttu-id="9e66a-146">複合</span><span class="sxs-lookup"><span data-stu-id="9e66a-146">Composites</span></span> |
| --- | --- |
| <span data-ttu-id="9e66a-147">xy</span><span class="sxs-lookup"><span data-stu-id="9e66a-147">xy</span></span> | <span data-ttu-id="9e66a-148">x 後接 y</span><span class="sxs-lookup"><span data-stu-id="9e66a-148">x followed by y</span></span> |
| <span data-ttu-id="9e66a-149">x\|y</span><span class="sxs-lookup"><span data-stu-id="9e66a-149">x\|y</span></span> | <span data-ttu-id="9e66a-150">x 或 y (偏好 x)</span><span class="sxs-lookup"><span data-stu-id="9e66a-150">x or y (prefer x)</span></span> |

| | <span data-ttu-id="9e66a-151">重複</span><span class="sxs-lookup"><span data-stu-id="9e66a-151">Repetitions</span></span> |
| --- | --- |
| <span data-ttu-id="9e66a-152">x\*</span><span class="sxs-lookup"><span data-stu-id="9e66a-152">x\*</span></span> | <span data-ttu-id="9e66a-153">零或多個 x，偏好更多</span><span class="sxs-lookup"><span data-stu-id="9e66a-153">zero or more x, prefer more</span></span> |
| <span data-ttu-id="9e66a-154">x+</span><span class="sxs-lookup"><span data-stu-id="9e66a-154">x+</span></span> | <span data-ttu-id="9e66a-155">一個或多個 x，偏好更多</span><span class="sxs-lookup"><span data-stu-id="9e66a-155">one or more x, prefer more</span></span> |
| <span data-ttu-id="9e66a-156">x?</span><span class="sxs-lookup"><span data-stu-id="9e66a-156">x?</span></span> | <span data-ttu-id="9e66a-157">零或一個 x，偏好更多</span><span class="sxs-lookup"><span data-stu-id="9e66a-157">zero or one x, prefer one</span></span> |
| <span data-ttu-id="9e66a-158">x{n,m}</span><span class="sxs-lookup"><span data-stu-id="9e66a-158">x{n,m}</span></span> | <span data-ttu-id="9e66a-159">n 或 n+1 或 ... 或 m x，偏好更多</span><span class="sxs-lookup"><span data-stu-id="9e66a-159">n or n+1 or ... or m x, prefer more</span></span> |
| <span data-ttu-id="9e66a-160">x{n,}</span><span class="sxs-lookup"><span data-stu-id="9e66a-160">x{n,}</span></span> | <span data-ttu-id="9e66a-161">n 或更多 x，偏好更多</span><span class="sxs-lookup"><span data-stu-id="9e66a-161">n or more x, prefer more</span></span> |
| <span data-ttu-id="9e66a-162">x{n}</span><span class="sxs-lookup"><span data-stu-id="9e66a-162">x{n}</span></span> | <span data-ttu-id="9e66a-163">完全符合 n x</span><span class="sxs-lookup"><span data-stu-id="9e66a-163">exactly n x</span></span> |
| <span data-ttu-id="9e66a-164">x\*?</span><span class="sxs-lookup"><span data-stu-id="9e66a-164">x\*?</span></span> | <span data-ttu-id="9e66a-165">零或多個 x，偏好更少</span><span class="sxs-lookup"><span data-stu-id="9e66a-165">zero or more x, prefer fewer</span></span> |
| <span data-ttu-id="9e66a-166">x+?</span><span class="sxs-lookup"><span data-stu-id="9e66a-166">x+?</span></span> | <span data-ttu-id="9e66a-167">一個或多個 x，偏好更少</span><span class="sxs-lookup"><span data-stu-id="9e66a-167">one or more x, prefer fewer</span></span> |
| <span data-ttu-id="9e66a-168">x??</span><span class="sxs-lookup"><span data-stu-id="9e66a-168">x??</span></span> | <span data-ttu-id="9e66a-169">零或一個 x，偏好零</span><span class="sxs-lookup"><span data-stu-id="9e66a-169">zero or one x, prefer zero</span></span> |
| <span data-ttu-id="9e66a-170">x{n,m}?</span><span class="sxs-lookup"><span data-stu-id="9e66a-170">x{n,m}?</span></span> | <span data-ttu-id="9e66a-171">n 或 n+1 或 ... 或 m x，偏好更少</span><span class="sxs-lookup"><span data-stu-id="9e66a-171">n or n+1 or ... or m x, prefer fewer</span></span> |
| <span data-ttu-id="9e66a-172">x{n,}?</span><span class="sxs-lookup"><span data-stu-id="9e66a-172">x{n,}?</span></span> | <span data-ttu-id="9e66a-173">n 或更多 x，偏好更少</span><span class="sxs-lookup"><span data-stu-id="9e66a-173">n or more x, prefer fewer</span></span> |
| <span data-ttu-id="9e66a-174">x{n}?</span><span class="sxs-lookup"><span data-stu-id="9e66a-174">x{n}?</span></span> | <span data-ttu-id="9e66a-175">完全符合 n x</span><span class="sxs-lookup"><span data-stu-id="9e66a-175">exactly n x</span></span> |
| <span data-ttu-id="9e66a-176">x{}</span><span class="sxs-lookup"><span data-stu-id="9e66a-176">x{}</span></span> | <span data-ttu-id="9e66a-177">(≡ x\*) (不支援) VIM</span><span class="sxs-lookup"><span data-stu-id="9e66a-177">(≡ x\*) (NOT SUPPORTED) VIM</span></span> |
| <span data-ttu-id="9e66a-178">x{-}</span><span class="sxs-lookup"><span data-stu-id="9e66a-178">x{-}</span></span> | <span data-ttu-id="9e66a-179">(≡ x\*?) (不支援) VIM</span><span class="sxs-lookup"><span data-stu-id="9e66a-179">(≡ x\*?) (NOT SUPPORTED) VIM</span></span> |
| <span data-ttu-id="9e66a-180">x{-n}</span><span class="sxs-lookup"><span data-stu-id="9e66a-180">x{-n}</span></span> | <span data-ttu-id="9e66a-181">(≡ x{n}?) (不支援) VIM</span><span class="sxs-lookup"><span data-stu-id="9e66a-181">(≡ x{n}?) (NOT SUPPORTED) VIM</span></span> |
| <span data-ttu-id="9e66a-182">x=</span><span class="sxs-lookup"><span data-stu-id="9e66a-182">x=</span></span> | <span data-ttu-id="9e66a-183">(≡ x?) (不支援) VIM</span><span class="sxs-lookup"><span data-stu-id="9e66a-183">(≡ x?) (NOT SUPPORTED) VIM</span></span> |

<span data-ttu-id="9e66a-184">實作限制：計算表單 x {n,m}，x {n,} 和 x {n} 拒絕創建最小或最大重複計數超過 1000 的表單。</span><span class="sxs-lookup"><span data-stu-id="9e66a-184">Implementation restriction: The counting forms x{n,m}, x{n,}, and x{n} reject forms that create a minimum or maximum repetition count above 1000.</span></span> <span data-ttu-id="9e66a-185">無限重複不受此限制。</span><span class="sxs-lookup"><span data-stu-id="9e66a-185">Unlimited repetitions are not subject to this restriction.</span></span>

| | <span data-ttu-id="9e66a-186">所有格重複</span><span class="sxs-lookup"><span data-stu-id="9e66a-186">Possessive repetitions</span></span> |
| --- | --- |
| <span data-ttu-id="9e66a-187">x\*+</span><span class="sxs-lookup"><span data-stu-id="9e66a-187">x\*+</span></span> | <span data-ttu-id="9e66a-188">零個或多個 x、所有格 (不支援)</span><span class="sxs-lookup"><span data-stu-id="9e66a-188">zero or more x, possessive (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="9e66a-189">x++</span><span class="sxs-lookup"><span data-stu-id="9e66a-189">x++</span></span> | <span data-ttu-id="9e66a-190">一或多個 x、所有格 (不支援)</span><span class="sxs-lookup"><span data-stu-id="9e66a-190">one or more x, possessive (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="9e66a-191">x?+</span><span class="sxs-lookup"><span data-stu-id="9e66a-191">x?+</span></span> | <span data-ttu-id="9e66a-192">零個或一個 x、所有格 (不支援)</span><span class="sxs-lookup"><span data-stu-id="9e66a-192">zero or one x, possessive (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="9e66a-193">x{n,m}+</span><span class="sxs-lookup"><span data-stu-id="9e66a-193">x{n,m}+</span></span> | <span data-ttu-id="9e66a-194">n 或 ... 或 m x，所有格 (不支持)</span><span class="sxs-lookup"><span data-stu-id="9e66a-194">n or ... or m x, possessive (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="9e66a-195">x{n,}+</span><span class="sxs-lookup"><span data-stu-id="9e66a-195">x{n,}+</span></span> | <span data-ttu-id="9e66a-196">n 或多個 x，所有格 (不支援)</span><span class="sxs-lookup"><span data-stu-id="9e66a-196">n or more x, possessive (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="9e66a-197">x{n}+</span><span class="sxs-lookup"><span data-stu-id="9e66a-197">x{n}+</span></span> | <span data-ttu-id="9e66a-198">完全符合 n x，所有格 (不支持)</span><span class="sxs-lookup"><span data-stu-id="9e66a-198">exactly n x, possessive (NOT SUPPORTED)</span></span> |

| | <span data-ttu-id="9e66a-199">分組</span><span class="sxs-lookup"><span data-stu-id="9e66a-199">Grouping</span></span> |
| --- | --- |
| <span data-ttu-id="9e66a-200">(re)</span><span class="sxs-lookup"><span data-stu-id="9e66a-200">(re)</span></span> | <span data-ttu-id="9e66a-201">編號擷取群組 (子符合)</span><span class="sxs-lookup"><span data-stu-id="9e66a-201">numbered capturing group (submatch)</span></span> |
| <span data-ttu-id="9e66a-202">(?P&lt;名稱&gt;re)</span><span class="sxs-lookup"><span data-stu-id="9e66a-202">(?P&lt;name&gt;re)</span></span> | <span data-ttu-id="9e66a-203">具名&amp;編號擷取群組 (子符合)</span><span class="sxs-lookup"><span data-stu-id="9e66a-203">named &amp; numbered capturing group (submatch)</span></span> |
| <span data-ttu-id="9e66a-204">(?&lt;名稱&gt;re)</span><span class="sxs-lookup"><span data-stu-id="9e66a-204">(?&lt;name&gt;re)</span></span> | <span data-ttu-id="9e66a-205">具名 &amp; 編號擷取群組 (子符合) (不支援)</span><span class="sxs-lookup"><span data-stu-id="9e66a-205">named &amp; numbered capturing group (submatch) (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="9e66a-206">(?&#39;name&#39;re)</span><span class="sxs-lookup"><span data-stu-id="9e66a-206">(?&#39;name&#39;re)</span></span> | <span data-ttu-id="9e66a-207">具名 &amp; 編號擷取群組 (子符合) (不支援)</span><span class="sxs-lookup"><span data-stu-id="9e66a-207">named &amp; numbered capturing group (submatch) (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="9e66a-208">(?:re)</span><span class="sxs-lookup"><span data-stu-id="9e66a-208">(?:re)</span></span> | <span data-ttu-id="9e66a-209">非擷取群組</span><span class="sxs-lookup"><span data-stu-id="9e66a-209">non-capturing group</span></span> |
| <span data-ttu-id="9e66a-210">(?flags)</span><span class="sxs-lookup"><span data-stu-id="9e66a-210">(?flags)</span></span> | <span data-ttu-id="9e66a-211">在目前的群組內設定旗標；非擷取</span><span class="sxs-lookup"><span data-stu-id="9e66a-211">set flags within current group; non-capturing</span></span> |
| <span data-ttu-id="9e66a-212">(?flags:re)</span><span class="sxs-lookup"><span data-stu-id="9e66a-212">(?flags:re)</span></span> | <span data-ttu-id="9e66a-213">在 re 期間設定旗標；非擷取</span><span class="sxs-lookup"><span data-stu-id="9e66a-213">set flags during re; non-capturing</span></span> |
| <span data-ttu-id="9e66a-214">(?#text)</span><span class="sxs-lookup"><span data-stu-id="9e66a-214">(?#text)</span></span> | <span data-ttu-id="9e66a-215">注釋 (不支援)</span><span class="sxs-lookup"><span data-stu-id="9e66a-215">comment (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="9e66a-216">(?\|x\|y\|z)</span><span class="sxs-lookup"><span data-stu-id="9e66a-216">(?\|x\|y\|z)</span></span> | <span data-ttu-id="9e66a-217">分支編號重設 (不支援)</span><span class="sxs-lookup"><span data-stu-id="9e66a-217">branch numbering reset (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="9e66a-218">(?&gt;re)</span><span class="sxs-lookup"><span data-stu-id="9e66a-218">(?&gt;re)</span></span> | <span data-ttu-id="9e66a-219">re 的所有格匹配 (不支持)</span><span class="sxs-lookup"><span data-stu-id="9e66a-219">possessive match of re (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="9e66a-220">re@&gt;</span><span class="sxs-lookup"><span data-stu-id="9e66a-220">re@&gt;</span></span> | <span data-ttu-id="9e66a-221">re 的所有格匹配 (不支援) VIM</span><span class="sxs-lookup"><span data-stu-id="9e66a-221">possessive match of re (NOT SUPPORTED) VIM</span></span> |
| <span data-ttu-id="9e66a-222">%(re)</span><span class="sxs-lookup"><span data-stu-id="9e66a-222">%(re)</span></span> | <span data-ttu-id="9e66a-223">非擷取群組 (不支援) VIM</span><span class="sxs-lookup"><span data-stu-id="9e66a-223">non-capturing group (NOT SUPPORTED) VIM</span></span> |

| | <span data-ttu-id="9e66a-224">Flags</span><span class="sxs-lookup"><span data-stu-id="9e66a-224">Flags</span></span> |
| --- | --- |
| <span data-ttu-id="9e66a-225">i</span><span class="sxs-lookup"><span data-stu-id="9e66a-225">i</span></span> | <span data-ttu-id="9e66a-226">不區分大小寫 (預設為 false)</span><span class="sxs-lookup"><span data-stu-id="9e66a-226">case-insensitive (default false)</span></span> |
| <span data-ttu-id="9e66a-227">m</span><span class="sxs-lookup"><span data-stu-id="9e66a-227">m</span></span> | <span data-ttu-id="9e66a-228">多行模式：除了開始/結束文字 (預設為 false) 以外，還能有 ^ 和 $ 符合開始/結束行。</span><span class="sxs-lookup"><span data-stu-id="9e66a-228">multi-line mode: ^ and $ match begin/end line in addition to begin/end text (default false)</span></span> |
| <span data-ttu-id="9e66a-229">s</span><span class="sxs-lookup"><span data-stu-id="9e66a-229">s</span></span> | <span data-ttu-id="9e66a-230">let .</span><span class="sxs-lookup"><span data-stu-id="9e66a-230">let .</span></span> <span data-ttu-id="9e66a-231">符合 \n (預設為 false)</span><span class="sxs-lookup"><span data-stu-id="9e66a-231">match \n (default false)</span></span> |
| <span data-ttu-id="9e66a-232">U</span><span class="sxs-lookup"><span data-stu-id="9e66a-232">U</span></span> | <span data-ttu-id="9e66a-233">ungreedy：交換 x\* 和 x\*?、x+ 和 x+? 等的意義 (預設為 false)</span><span class="sxs-lookup"><span data-stu-id="9e66a-233">ungreedy: swap meaning of x\* and x\*?, x+ and x+?, etc (default false)</span></span> |

<span data-ttu-id="9e66a-234">旗標語法為 xyz (set) 或 -xyz (clear) 或 xy-z (設定為 xy、clear z)。</span><span class="sxs-lookup"><span data-stu-id="9e66a-234">Flag syntax is xyz (set) or -xyz (clear) or xy-z (set xy, clear z).</span></span>

|  | <span data-ttu-id="9e66a-235">空字串</span><span class="sxs-lookup"><span data-stu-id="9e66a-235">Empty strings</span></span> |
| --- | --- |
| ^ | <span data-ttu-id="9e66a-236">文字或行的開頭 (m=true)</span><span class="sxs-lookup"><span data-stu-id="9e66a-236">at beginning of text or line (m=true)</span></span> |
| $ | <span data-ttu-id="9e66a-237">文字 (例如 \z 非 \Z) 或行的結尾 (m=true)</span><span class="sxs-lookup"><span data-stu-id="9e66a-237">at end of text (like \z not \Z) or line (m=true)</span></span> |
| <span data-ttu-id="9e66a-238">\A</span><span class="sxs-lookup"><span data-stu-id="9e66a-238">\A</span></span> | <span data-ttu-id="9e66a-239">文字的開頭</span><span class="sxs-lookup"><span data-stu-id="9e66a-239">at beginning of text</span></span> |
| <span data-ttu-id="9e66a-240">\b</span><span class="sxs-lookup"><span data-stu-id="9e66a-240">\b</span></span> | <span data-ttu-id="9e66a-241">在 ASCII 字的邊界 (一邊是\w，另一邊是 \W, \A, or \z)</span><span class="sxs-lookup"><span data-stu-id="9e66a-241">at ASCII word boundary (\w on one side and \W, \A, or \z on the other)</span></span> |
| <span data-ttu-id="9e66a-242">\B</span><span class="sxs-lookup"><span data-stu-id="9e66a-242">\B</span></span> | <span data-ttu-id="9e66a-243">不在 ASCII 字的邊界</span><span class="sxs-lookup"><span data-stu-id="9e66a-243">not at ASCII word boundary</span></span> |
| <span data-ttu-id="9e66a-244">\g</span><span class="sxs-lookup"><span data-stu-id="9e66a-244">\g</span></span> | <span data-ttu-id="9e66a-245">搜尋的次文字的開頭處 (不支援) PCRE</span><span class="sxs-lookup"><span data-stu-id="9e66a-245">at beginning of subtext being searched (NOT SUPPORTED) PCRE</span></span> |
| <span data-ttu-id="9e66a-246">\G</span><span class="sxs-lookup"><span data-stu-id="9e66a-246">\G</span></span> | <span data-ttu-id="9e66a-247">最近符合的結尾處 (不支援) PERL</span><span class="sxs-lookup"><span data-stu-id="9e66a-247">at end of last match (NOT SUPPORTED) PERL</span></span> |
| <span data-ttu-id="9e66a-248">\Z</span><span class="sxs-lookup"><span data-stu-id="9e66a-248">\Z</span></span> | <span data-ttu-id="9e66a-249">在文字結尾處，或文字結尾處的新行字元之前 (不支援)</span><span class="sxs-lookup"><span data-stu-id="9e66a-249">at end of text, or before newline at end of text (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="9e66a-250">\z</span><span class="sxs-lookup"><span data-stu-id="9e66a-250">\z</span></span> | <span data-ttu-id="9e66a-251">在文字結尾處</span><span class="sxs-lookup"><span data-stu-id="9e66a-251">at end of text</span></span> |
| <span data-ttu-id="9e66a-252">(?=re)</span><span class="sxs-lookup"><span data-stu-id="9e66a-252">(?=re)</span></span> | <span data-ttu-id="9e66a-253">在文字與 re 相符之前 (不支援)</span><span class="sxs-lookup"><span data-stu-id="9e66a-253">before text matching re (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="9e66a-254">(?!re)</span><span class="sxs-lookup"><span data-stu-id="9e66a-254">(?!re)</span></span> | <span data-ttu-id="9e66a-255">在文字不符合 re 之前 (不支援)</span><span class="sxs-lookup"><span data-stu-id="9e66a-255">before text not matching re (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="9e66a-256">(?&lt;=re)</span><span class="sxs-lookup"><span data-stu-id="9e66a-256">(?&lt;=re)</span></span> | <span data-ttu-id="9e66a-257">在文字與 re 相符之后 (不支援)</span><span class="sxs-lookup"><span data-stu-id="9e66a-257">after text matching re (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="9e66a-258">(?&lt;!re)</span><span class="sxs-lookup"><span data-stu-id="9e66a-258">(?&lt;!re)</span></span> | <span data-ttu-id="9e66a-259">在文字與 re 不相符之后 (不支援)</span><span class="sxs-lookup"><span data-stu-id="9e66a-259">after text not matching re (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="9e66a-260">re&amp;</span><span class="sxs-lookup"><span data-stu-id="9e66a-260">re&amp;</span></span> | <span data-ttu-id="9e66a-261">在文字與 re 相符之前 (不支援) VIM</span><span class="sxs-lookup"><span data-stu-id="9e66a-261">before text matching re (NOT SUPPORTED) VIM</span></span> |
| <span data-ttu-id="9e66a-262">re@=</span><span class="sxs-lookup"><span data-stu-id="9e66a-262">re@=</span></span> | <span data-ttu-id="9e66a-263">在文字與 re 相符之前 (不支援) VIM</span><span class="sxs-lookup"><span data-stu-id="9e66a-263">before text matching re (NOT SUPPORTED) VIM</span></span> |
| <span data-ttu-id="9e66a-264">re@!</span><span class="sxs-lookup"><span data-stu-id="9e66a-264">re@!</span></span> | <span data-ttu-id="9e66a-265">在文字不符合 re 之前 (不支援) VIM</span><span class="sxs-lookup"><span data-stu-id="9e66a-265">before text not matching re (NOT SUPPORTED) VIM</span></span> |
| <span data-ttu-id="9e66a-266">re@&lt;=</span><span class="sxs-lookup"><span data-stu-id="9e66a-266">re@&lt;=</span></span> | <span data-ttu-id="9e66a-267">在文字與 re 相符之后 (不支援) VIM</span><span class="sxs-lookup"><span data-stu-id="9e66a-267">after text matching re (NOT SUPPORTED) VIM</span></span> |
| <span data-ttu-id="9e66a-268">re@&lt;!</span><span class="sxs-lookup"><span data-stu-id="9e66a-268">re@&lt;!</span></span> | <span data-ttu-id="9e66a-269">在文字與 re 不相符之后 (不支援) VIM</span><span class="sxs-lookup"><span data-stu-id="9e66a-269">after text not matching re (NOT SUPPORTED) VIM</span></span> |
| <span data-ttu-id="9e66a-270">\zs</span><span class="sxs-lookup"><span data-stu-id="9e66a-270">\zs</span></span> | <span data-ttu-id="9e66a-271">開始匹配組 (= \K) (不支援) VIM</span><span class="sxs-lookup"><span data-stu-id="9e66a-271">sets start of match (= \K) (NOT SUPPORTED) VIM</span></span> |
| <span data-ttu-id="9e66a-272">\ze</span><span class="sxs-lookup"><span data-stu-id="9e66a-272">\ze</span></span> | <span data-ttu-id="9e66a-273">結束匹配組 (不支援) VIM</span><span class="sxs-lookup"><span data-stu-id="9e66a-273">sets end of match (NOT SUPPORTED) VIM</span></span> |
| \%^ | <span data-ttu-id="9e66a-274">檔案開頭 (不支援) VIM</span><span class="sxs-lookup"><span data-stu-id="9e66a-274">beginning of file (NOT SUPPORTED) VIM</span></span> |
| \%$ | <span data-ttu-id="9e66a-275">檔案結尾 (不支持) VIM</span><span class="sxs-lookup"><span data-stu-id="9e66a-275">end of file (NOT SUPPORTED) VIM</span></span> |
| <span data-ttu-id="9e66a-276">\%V</span><span class="sxs-lookup"><span data-stu-id="9e66a-276">\%V</span></span> | <span data-ttu-id="9e66a-277">在螢幕上 (不支援) VIM</span><span class="sxs-lookup"><span data-stu-id="9e66a-277">on screen (NOT SUPPORTED) VIM</span></span> |
| \%# | <span data-ttu-id="9e66a-278">游標位置 (不支援) VIM</span><span class="sxs-lookup"><span data-stu-id="9e66a-278">cursor position (NOT SUPPORTED) VIM</span></span> |
| <span data-ttu-id="9e66a-279">\%&#39;m</span><span class="sxs-lookup"><span data-stu-id="9e66a-279">\%&#39;m</span></span> | <span data-ttu-id="9e66a-280">標記 m 位置 (不支援) VIM</span><span class="sxs-lookup"><span data-stu-id="9e66a-280">mark m position (NOT SUPPORTED) VIM</span></span> |
| <span data-ttu-id="9e66a-281">\%23l</span><span class="sxs-lookup"><span data-stu-id="9e66a-281">\%23l</span></span> | <span data-ttu-id="9e66a-282">在行 23 中 (不支援) VIM</span><span class="sxs-lookup"><span data-stu-id="9e66a-282">in line 23 (NOT SUPPORTED) VIM</span></span> |
| <span data-ttu-id="9e66a-283">\%23c</span><span class="sxs-lookup"><span data-stu-id="9e66a-283">\%23c</span></span> | <span data-ttu-id="9e66a-284">在欄 23 中 (不支援) VIM </span><span class="sxs-lookup"><span data-stu-id="9e66a-284">in column 23 (NOT SUPPORTED) VIM</span></span> |
| <span data-ttu-id="9e66a-285">\%23v</span><span class="sxs-lookup"><span data-stu-id="9e66a-285">\%23v</span></span> | <span data-ttu-id="9e66a-286">在虛擬欄 23 中 (不支援) VIM</span><span class="sxs-lookup"><span data-stu-id="9e66a-286">in virtual column 23 (NOT SUPPORTED) VIM</span></span> |

|  | <span data-ttu-id="9e66a-287">逸出序列</span><span class="sxs-lookup"><span data-stu-id="9e66a-287">Escape sequences</span></span> |
| --- | --- |
| <span data-ttu-id="9e66a-288">\a</span><span class="sxs-lookup"><span data-stu-id="9e66a-288">\a</span></span> | <span data-ttu-id="9e66a-289">bell (≡ \007)</span><span class="sxs-lookup"><span data-stu-id="9e66a-289">bell (≡ \007)</span></span> |
| <span data-ttu-id="9e66a-290">\f</span><span class="sxs-lookup"><span data-stu-id="9e66a-290">\f</span></span> | <span data-ttu-id="9e66a-291">表單摘要 (≡ \014)</span><span class="sxs-lookup"><span data-stu-id="9e66a-291">form feed (≡ \014)</span></span> |
| <span data-ttu-id="9e66a-292">\t</span><span class="sxs-lookup"><span data-stu-id="9e66a-292">\t</span></span> | <span data-ttu-id="9e66a-293">水平索引標籤 (≡ \011)</span><span class="sxs-lookup"><span data-stu-id="9e66a-293">horizontal tab (≡ \011)</span></span> |
| <span data-ttu-id="9e66a-294">\n</span><span class="sxs-lookup"><span data-stu-id="9e66a-294">\n</span></span> | <span data-ttu-id="9e66a-295">新行字元 (≡ \012)</span><span class="sxs-lookup"><span data-stu-id="9e66a-295">newline (≡ \012)</span></span> |
| <span data-ttu-id="9e66a-296">\r</span><span class="sxs-lookup"><span data-stu-id="9e66a-296">\r</span></span> | <span data-ttu-id="9e66a-297">滑動架傳回 (≡ \015)</span><span class="sxs-lookup"><span data-stu-id="9e66a-297">carriage return (≡ \015)</span></span> |
| <span data-ttu-id="9e66a-298">\v</span><span class="sxs-lookup"><span data-stu-id="9e66a-298">\v</span></span> | <span data-ttu-id="9e66a-299">垂直定位字元 (≡ \013)</span><span class="sxs-lookup"><span data-stu-id="9e66a-299">vertical tab character (≡ \013)</span></span> |
| \* | <span data-ttu-id="9e66a-300">常值 \*，適用于任何標點字元 \*</span><span class="sxs-lookup"><span data-stu-id="9e66a-300">literal \*, for any punctuation character \*</span></span> |
| <span data-ttu-id="9e66a-301">\123</span><span class="sxs-lookup"><span data-stu-id="9e66a-301">\123</span></span> | <span data-ttu-id="9e66a-302">八進位字元代碼 (最多三個數字)</span><span class="sxs-lookup"><span data-stu-id="9e66a-302">octal character code (up to three digits)</span></span> |
| <span data-ttu-id="9e66a-303">\x7F</span><span class="sxs-lookup"><span data-stu-id="9e66a-303">\x7F</span></span> | <span data-ttu-id="9e66a-304">十六進位字元碼 (正好兩個數字)</span><span class="sxs-lookup"><span data-stu-id="9e66a-304">hex character code (exactly two digits)</span></span> |
| <span data-ttu-id="9e66a-305">\x{10FFFF}</span><span class="sxs-lookup"><span data-stu-id="9e66a-305">\x{10FFFF}</span></span> | <span data-ttu-id="9e66a-306">十六進位字元代碼</span><span class="sxs-lookup"><span data-stu-id="9e66a-306">hex character code</span></span> |
| <span data-ttu-id="9e66a-307">\C</span><span class="sxs-lookup"><span data-stu-id="9e66a-307">\C</span></span> | <span data-ttu-id="9e66a-308">即使在 UTF-8 模式中也與單一位元組相符</span><span class="sxs-lookup"><span data-stu-id="9e66a-308">match a single byte even in UTF-8 mode</span></span> |
| <span data-ttu-id="9e66a-309">\Q...\E</span><span class="sxs-lookup"><span data-stu-id="9e66a-309">\Q...\E</span></span> | <span data-ttu-id="9e66a-310">常值文字 ... 即使 ... 有標點符號</span><span class="sxs-lookup"><span data-stu-id="9e66a-310">literal text ... even if ... has punctuation</span></span> |
| <span data-ttu-id="9e66a-311">\1</span><span class="sxs-lookup"><span data-stu-id="9e66a-311">\1</span></span> | <span data-ttu-id="9e66a-312">反向參考 (不支援)</span><span class="sxs-lookup"><span data-stu-id="9e66a-312">backreference (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="9e66a-313">\b</span><span class="sxs-lookup"><span data-stu-id="9e66a-313">\b</span></span> | <span data-ttu-id="9e66a-314">退格鍵 (不支援) (使用 \ 010)</span><span class="sxs-lookup"><span data-stu-id="9e66a-314">backspace (NOT SUPPORTED) (use \010)</span></span> |
| <span data-ttu-id="9e66a-315">\cK</span><span class="sxs-lookup"><span data-stu-id="9e66a-315">\cK</span></span> | <span data-ttu-id="9e66a-316">控制 char ^K (不支援) (使用 \001 等)</span><span class="sxs-lookup"><span data-stu-id="9e66a-316">control char ^K (NOT SUPPORTED) (use \001 etc)</span></span> |
| <span data-ttu-id="9e66a-317">\e</span><span class="sxs-lookup"><span data-stu-id="9e66a-317">\e</span></span> | <span data-ttu-id="9e66a-318">逸出 (不支援) (使用 \033)</span><span class="sxs-lookup"><span data-stu-id="9e66a-318">escape (NOT SUPPORTED) (use \033)</span></span> |
| <span data-ttu-id="9e66a-319">\g1</span><span class="sxs-lookup"><span data-stu-id="9e66a-319">\g1</span></span> | <span data-ttu-id="9e66a-320">反向參考 (不支援)</span><span class="sxs-lookup"><span data-stu-id="9e66a-320">backreference (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="9e66a-321">\g{1}</span><span class="sxs-lookup"><span data-stu-id="9e66a-321">\g{1}</span></span> | <span data-ttu-id="9e66a-322">反向參考 (不支援)</span><span class="sxs-lookup"><span data-stu-id="9e66a-322">backreference (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="9e66a-323">\g{+1}</span><span class="sxs-lookup"><span data-stu-id="9e66a-323">\g{+1}</span></span> | <span data-ttu-id="9e66a-324">反向參考 (不支援)</span><span class="sxs-lookup"><span data-stu-id="9e66a-324">backreference (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="9e66a-325">\g{-1}</span><span class="sxs-lookup"><span data-stu-id="9e66a-325">\g{-1}</span></span> | <span data-ttu-id="9e66a-326">反向參考 (不支援)</span><span class="sxs-lookup"><span data-stu-id="9e66a-326">backreference (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="9e66a-327">\g{name}</span><span class="sxs-lookup"><span data-stu-id="9e66a-327">\g{name}</span></span> | <span data-ttu-id="9e66a-328">具名反向參考 (不支援)</span><span class="sxs-lookup"><span data-stu-id="9e66a-328">named backreference (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="9e66a-329">\g&lt;名稱&gt;</span><span class="sxs-lookup"><span data-stu-id="9e66a-329">\g&lt;name&gt;</span></span> | <span data-ttu-id="9e66a-330">副程式撥號 (不支援)</span><span class="sxs-lookup"><span data-stu-id="9e66a-330">subroutine call (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="9e66a-331">\g&#39;name&#39;</span><span class="sxs-lookup"><span data-stu-id="9e66a-331">\g&#39;name&#39;</span></span> | <span data-ttu-id="9e66a-332">副程式撥號 (不支援)</span><span class="sxs-lookup"><span data-stu-id="9e66a-332">subroutine call (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="9e66a-333">\k&lt;名稱&gt;</span><span class="sxs-lookup"><span data-stu-id="9e66a-333">\k&lt;name&gt;</span></span> | <span data-ttu-id="9e66a-334">具名反向參考 (不支援)</span><span class="sxs-lookup"><span data-stu-id="9e66a-334">named backreference (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="9e66a-335">\k&#39;name&#39;</span><span class="sxs-lookup"><span data-stu-id="9e66a-335">\k&#39;name&#39;</span></span> | <span data-ttu-id="9e66a-336">具名反向參考 (不支援)</span><span class="sxs-lookup"><span data-stu-id="9e66a-336">named backreference (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="9e66a-337">\lX</span><span class="sxs-lookup"><span data-stu-id="9e66a-337">\lX</span></span> | <span data-ttu-id="9e66a-338">小寫 X (不支援)</span><span class="sxs-lookup"><span data-stu-id="9e66a-338">lowercase X (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="9e66a-339">\ux</span><span class="sxs-lookup"><span data-stu-id="9e66a-339">\ux</span></span> | <span data-ttu-id="9e66a-340">大寫 x (不支持)</span><span class="sxs-lookup"><span data-stu-id="9e66a-340">uppercase x (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="9e66a-341">\L...\E</span><span class="sxs-lookup"><span data-stu-id="9e66a-341">\L...\E</span></span> | <span data-ttu-id="9e66a-342">小寫文字 ... (不支援)</span><span class="sxs-lookup"><span data-stu-id="9e66a-342">lowercase text ... (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="9e66a-343">\K</span><span class="sxs-lookup"><span data-stu-id="9e66a-343">\K</span></span> | <span data-ttu-id="9e66a-344">重設 $0 的開頭 (不支援)</span><span class="sxs-lookup"><span data-stu-id="9e66a-344">reset beginning of $0 (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="9e66a-345">\N{name}</span><span class="sxs-lookup"><span data-stu-id="9e66a-345">\N{name}</span></span> | <span data-ttu-id="9e66a-346">具名 Unicode 字元 (不支援)</span><span class="sxs-lookup"><span data-stu-id="9e66a-346">named Unicode character (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="9e66a-347">\R</span><span class="sxs-lookup"><span data-stu-id="9e66a-347">\R</span></span> | <span data-ttu-id="9e66a-348">分行符號 (不支援)</span><span class="sxs-lookup"><span data-stu-id="9e66a-348">line break (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="9e66a-349">\U...\E</span><span class="sxs-lookup"><span data-stu-id="9e66a-349">\U...\E</span></span> | <span data-ttu-id="9e66a-350">大寫文字 ... (不支援)</span><span class="sxs-lookup"><span data-stu-id="9e66a-350">upper case text ... (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="9e66a-351">\X</span><span class="sxs-lookup"><span data-stu-id="9e66a-351">\X</span></span> | <span data-ttu-id="9e66a-352">擴充 Unicode 序列 (不支援)</span><span class="sxs-lookup"><span data-stu-id="9e66a-352">extended Unicode sequence (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="9e66a-353">\%d123</span><span class="sxs-lookup"><span data-stu-id="9e66a-353">\%d123</span></span> | <span data-ttu-id="9e66a-354">十進位字元 123 (不支援) VIM</span><span class="sxs-lookup"><span data-stu-id="9e66a-354">decimal character 123 (NOT SUPPORTED) VIM</span></span> |
| <span data-ttu-id="9e66a-355">\%xFF</span><span class="sxs-lookup"><span data-stu-id="9e66a-355">\%xFF</span></span> | <span data-ttu-id="9e66a-356">十六進位字元 FF (不支援) VIM</span><span class="sxs-lookup"><span data-stu-id="9e66a-356">hex character FF (NOT SUPPORTED) VIM</span></span> |
| <span data-ttu-id="9e66a-357">\%o123</span><span class="sxs-lookup"><span data-stu-id="9e66a-357">\%o123</span></span> | <span data-ttu-id="9e66a-358">八進位字元 123 (不支援) VIM</span><span class="sxs-lookup"><span data-stu-id="9e66a-358">octal character 123 (NOT SUPPORTED) VIM</span></span> |
| <span data-ttu-id="9e66a-359">\%u1234</span><span class="sxs-lookup"><span data-stu-id="9e66a-359">\%u1234</span></span> | <span data-ttu-id="9e66a-360">Unicode 字元 0x1234 (不支援) VIM</span><span class="sxs-lookup"><span data-stu-id="9e66a-360">Unicode character 0x1234 (NOT SUPPORTED) VIM</span></span> |
| <span data-ttu-id="9e66a-361">\%U12345678</span><span class="sxs-lookup"><span data-stu-id="9e66a-361">\%U12345678</span></span> | <span data-ttu-id="9e66a-362">Unicode 字元 0x12345678 (不支援) VIM</span><span class="sxs-lookup"><span data-stu-id="9e66a-362">Unicode character 0x12345678 (NOT SUPPORTED) VIM</span></span> |

|  | <span data-ttu-id="9e66a-363">字元類別元素</span><span class="sxs-lookup"><span data-stu-id="9e66a-363">Character class elements</span></span> |
| --- | --- |
| <span data-ttu-id="9e66a-364">x</span><span class="sxs-lookup"><span data-stu-id="9e66a-364">x</span></span> | <span data-ttu-id="9e66a-365">單一字元</span><span class="sxs-lookup"><span data-stu-id="9e66a-365">single character</span></span> |
| <span data-ttu-id="9e66a-366">A-Z</span><span class="sxs-lookup"><span data-stu-id="9e66a-366">A-Z</span></span> | <span data-ttu-id="9e66a-367">字元範圍 (全人)</span><span class="sxs-lookup"><span data-stu-id="9e66a-367">character range (inclusive)</span></span> |
| <span data-ttu-id="9e66a-368">\d</span><span class="sxs-lookup"><span data-stu-id="9e66a-368">\d</span></span> | <span data-ttu-id="9e66a-369">Perl 字元類別</span><span class="sxs-lookup"><span data-stu-id="9e66a-369">Perl character class</span></span> |
| <span data-ttu-id="9e66a-370">[:foo:]</span><span class="sxs-lookup"><span data-stu-id="9e66a-370">[:foo:]</span></span> | <span data-ttu-id="9e66a-371">ASCII 字元類別 foo</span><span class="sxs-lookup"><span data-stu-id="9e66a-371">ASCII character class foo</span></span> |
| <span data-ttu-id="9e66a-372">\p{Foo}</span><span class="sxs-lookup"><span data-stu-id="9e66a-372">\p{Foo}</span></span> | <span data-ttu-id="9e66a-373">Unicode 字元類別 Foo</span><span class="sxs-lookup"><span data-stu-id="9e66a-373">Unicode character class Foo</span></span> |
| <span data-ttu-id="9e66a-374">\pF</span><span class="sxs-lookup"><span data-stu-id="9e66a-374">\pF</span></span> | <span data-ttu-id="9e66a-375">Unicode 字元類別 F (單字母名稱)</span><span class="sxs-lookup"><span data-stu-id="9e66a-375">Unicode character class F (one-letter name)</span></span> |

|  | <span data-ttu-id="9e66a-376">具名字元類作為字元類元素</span><span class="sxs-lookup"><span data-stu-id="9e66a-376">Named character classes as character class elements</span></span> |
| --- | --- |
| <span data-ttu-id="9e66a-377">[\d]</span><span class="sxs-lookup"><span data-stu-id="9e66a-377">[\d]</span></span> | <span data-ttu-id="9e66a-378">數位 (≡ \d)</span><span class="sxs-lookup"><span data-stu-id="9e66a-378">digits (≡ \d)</span></span> |
| <span data-ttu-id="9e66a-379">[^\d]</span><span class="sxs-lookup"><span data-stu-id="9e66a-379">[^\d]</span></span> | <span data-ttu-id="9e66a-380">非數位 (≡ \D)</span><span class="sxs-lookup"><span data-stu-id="9e66a-380">not digits (≡ \D)</span></span> |
| <span data-ttu-id="9e66a-381">[\D]</span><span class="sxs-lookup"><span data-stu-id="9e66a-381">[\D]</span></span> | <span data-ttu-id="9e66a-382">非數位 (≡ \D)</span><span class="sxs-lookup"><span data-stu-id="9e66a-382">not digits (≡ \D)</span></span> |
| <span data-ttu-id="9e66a-383">[^\D]</span><span class="sxs-lookup"><span data-stu-id="9e66a-383">[^\D]</span></span> | <span data-ttu-id="9e66a-384">否非數位 (≡ \d)</span><span class="sxs-lookup"><span data-stu-id="9e66a-384">not not digits (≡ \d)</span></span> |
| <span data-ttu-id="9e66a-385">[[:name:]]</span><span class="sxs-lookup"><span data-stu-id="9e66a-385">[[:name:]]</span></span> | <span data-ttu-id="9e66a-386">字元類別中的具名 ASCII 類別 (≡ [:name:])</span><span class="sxs-lookup"><span data-stu-id="9e66a-386">named ASCII class inside character class (≡ [:name:])</span></span> |
| <span data-ttu-id="9e66a-387">[^[:name:]]</span><span class="sxs-lookup"><span data-stu-id="9e66a-387">[^[:name:]]</span></span> | <span data-ttu-id="9e66a-388">在反字元類中的具名 ASCII 類別 (≡ [:^name:])</span><span class="sxs-lookup"><span data-stu-id="9e66a-388">named ASCII class inside negated character class (≡ [:^name:])</span></span> |
| <span data-ttu-id="9e66a-389">[\p{Name}]</span><span class="sxs-lookup"><span data-stu-id="9e66a-389">[\p{Name}]</span></span> | <span data-ttu-id="9e66a-390">字元類別中的具名 Unicode 屬性 (≡ \p{Name})</span><span class="sxs-lookup"><span data-stu-id="9e66a-390">named Unicode property inside character class (≡ \p{Name})</span></span> |
| <span data-ttu-id="9e66a-391">[^\p{Name}]</span><span class="sxs-lookup"><span data-stu-id="9e66a-391">[^\p{Name}]</span></span> | <span data-ttu-id="9e66a-392">反字元類別中的具名 Unicode 屬性 (≡ \p{Name})</span><span class="sxs-lookup"><span data-stu-id="9e66a-392">named Unicode property inside negated character class (≡ \P{Name})</span></span> |

| <a name="user-content-perl"></a> | <span data-ttu-id="9e66a-393">Perl 字元類 (全為 ASCII)</span><span class="sxs-lookup"><span data-stu-id="9e66a-393">Perl character classes (all ASCII-only)</span></span> |
| --- | --- |
| <span data-ttu-id="9e66a-394">\d</span><span class="sxs-lookup"><span data-stu-id="9e66a-394">\d</span></span> | <span data-ttu-id="9e66a-395">位數 (≡ [0-9])</span><span class="sxs-lookup"><span data-stu-id="9e66a-395">digits (≡ [0-9])</span></span> |
| <span data-ttu-id="9e66a-396">\D</span><span class="sxs-lookup"><span data-stu-id="9e66a-396">\D</span></span> | <span data-ttu-id="9e66a-397">非位數 (≡ [^0-9])</span><span class="sxs-lookup"><span data-stu-id="9e66a-397">not digits (≡ [^0-9])</span></span> |
| <span data-ttu-id="9e66a-398">\s</span><span class="sxs-lookup"><span data-stu-id="9e66a-398">\s</span></span> | <span data-ttu-id="9e66a-399">空格 (≡ [\t\n\f\r])</span><span class="sxs-lookup"><span data-stu-id="9e66a-399">whitespace (≡ [\t\n\f\r])</span></span> |
| <span data-ttu-id="9e66a-400">\S</span><span class="sxs-lookup"><span data-stu-id="9e66a-400">\S</span></span> | <span data-ttu-id="9e66a-401">非空格 (≡ [^\t\n\f\r])</span><span class="sxs-lookup"><span data-stu-id="9e66a-401">not whitespace (≡ [^\t\n\f\r])</span></span> |
| <span data-ttu-id="9e66a-402">\w</span><span class="sxs-lookup"><span data-stu-id="9e66a-402">\w</span></span> | <span data-ttu-id="9e66a-403">文字字元 (≡ [0-9A-Za-z\_])</span><span class="sxs-lookup"><span data-stu-id="9e66a-403">word characters (≡ [0-9A-Za-z\_])</span></span> |
| <span data-ttu-id="9e66a-404">\W</span><span class="sxs-lookup"><span data-stu-id="9e66a-404">\W</span></span> | <span data-ttu-id="9e66a-405">非文字字元 (≡ [^0-9A-Za-z\_])</span><span class="sxs-lookup"><span data-stu-id="9e66a-405">not word characters (≡ [^0-9A-Za-z\_])</span></span> |
| <span data-ttu-id="9e66a-406">\h</span><span class="sxs-lookup"><span data-stu-id="9e66a-406">\h</span></span> | <span data-ttu-id="9e66a-407">水平空間 (不支援)</span><span class="sxs-lookup"><span data-stu-id="9e66a-407">horizontal space (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="9e66a-408">\H</span><span class="sxs-lookup"><span data-stu-id="9e66a-408">\H</span></span> | <span data-ttu-id="9e66a-409">非水平空間 (不支援)</span><span class="sxs-lookup"><span data-stu-id="9e66a-409">not horizontal space (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="9e66a-410">\v</span><span class="sxs-lookup"><span data-stu-id="9e66a-410">\v</span></span> | <span data-ttu-id="9e66a-411">垂直空間 (不支援)</span><span class="sxs-lookup"><span data-stu-id="9e66a-411">vertical space (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="9e66a-412">\V</span><span class="sxs-lookup"><span data-stu-id="9e66a-412">\V</span></span> | <span data-ttu-id="9e66a-413">非垂直空間 (不支援)</span><span class="sxs-lookup"><span data-stu-id="9e66a-413">not vertical space (NOT SUPPORTED)</span></span> |

|<a name="user-content-ascii"></a>  | <span data-ttu-id="9e66a-414">ASCII 字元類別</span><span class="sxs-lookup"><span data-stu-id="9e66a-414">ASCII character classes</span></span> |
| --- | --- |
| <span data-ttu-id="9e66a-415">[[:alnum:]]</span><span class="sxs-lookup"><span data-stu-id="9e66a-415">[[:alnum:]]</span></span> | <span data-ttu-id="9e66a-416">英數字元 (≡ [0-9A-Za-z])</span><span class="sxs-lookup"><span data-stu-id="9e66a-416">alphanumeric (≡ [0-9A-Za-z])</span></span> |
| <span data-ttu-id="9e66a-417">[[:alpha:]]</span><span class="sxs-lookup"><span data-stu-id="9e66a-417">[[:alpha:]]</span></span> | <span data-ttu-id="9e66a-418">字母 (≡ [A-Za-z])</span><span class="sxs-lookup"><span data-stu-id="9e66a-418">alphabetic (≡ [A-Za-z])</span></span> |
| <span data-ttu-id="9e66a-419">[[:ascii:]]</span><span class="sxs-lookup"><span data-stu-id="9e66a-419">[[:ascii:]]</span></span> | <span data-ttu-id="9e66a-420">ASCII (≡ [\x00-\x7F])</span><span class="sxs-lookup"><span data-stu-id="9e66a-420">ASCII (≡ [\x00-\x7F])</span></span> |
| <span data-ttu-id="9e66a-421">[[:blank:]]</span><span class="sxs-lookup"><span data-stu-id="9e66a-421">[[:blank:]]</span></span> | <span data-ttu-id="9e66a-422">空白(≡ [\t])</span><span class="sxs-lookup"><span data-stu-id="9e66a-422">blank (≡ [\t])</span></span> |
| <span data-ttu-id="9e66a-423">[[:cntrl:]]</span><span class="sxs-lookup"><span data-stu-id="9e66a-423">[[:cntrl:]]</span></span> | <span data-ttu-id="9e66a-424">控制項 (≡ [\x00-\x1F\x7F])</span><span class="sxs-lookup"><span data-stu-id="9e66a-424">control (≡ [\x00-\x1F\x7F])</span></span> |
| <span data-ttu-id="9e66a-425">[[:d igit：]]</span><span class="sxs-lookup"><span data-stu-id="9e66a-425">[[:digit:]]</span></span> | <span data-ttu-id="9e66a-426">位數 (≡ [0-9])</span><span class="sxs-lookup"><span data-stu-id="9e66a-426">digits (≡ [0-9])</span></span> |
| <span data-ttu-id="9e66a-427">[[:graph:]]</span><span class="sxs-lookup"><span data-stu-id="9e66a-427">[[:graph:]]</span></span> | <span data-ttu-id="9e66a-428">圖形化 (≡ `[!-~]` ≡ `[A-Za-z0-9!&quot;#$%&amp;&#39;()\*+,\-./:;&lt;=&gt;?@[\\\]^_`\` `{\|}~]`)</span><span class="sxs-lookup"><span data-stu-id="9e66a-428">graphical (≡ `[!-~]` ≡ `[A-Za-z0-9!&quot;#$%&amp;&#39;()\*+,\-./:;&lt;=&gt;?@[\\\]^_`\` `{\|}~]`)</span></span> |
| <span data-ttu-id="9e66a-429">[[:lower:]]</span><span class="sxs-lookup"><span data-stu-id="9e66a-429">[[:lower:]]</span></span> | <span data-ttu-id="9e66a-430">小寫 (≡ [a-z])</span><span class="sxs-lookup"><span data-stu-id="9e66a-430">lower case (≡ [a-z])</span></span> |
| <span data-ttu-id="9e66a-431">[[:print:]]</span><span class="sxs-lookup"><span data-stu-id="9e66a-431">[[:print:]]</span></span> | <span data-ttu-id="9e66a-432">可列印 (≡ [-~] ≡ [[:graph:]])</span><span class="sxs-lookup"><span data-stu-id="9e66a-432">printable (≡ [-~] ≡ [[:graph:]])</span></span> |
| <span data-ttu-id="9e66a-433">[[:punct:]]</span><span class="sxs-lookup"><span data-stu-id="9e66a-433">[[:punct:]]</span></span> | <span data-ttu-id="9e66a-434">標點符號 (≡ [!-/:-@[-\`{-~])</span><span class="sxs-lookup"><span data-stu-id="9e66a-434">punctuation (≡ [!-/:-@[-\`{-~])</span></span> |
| <span data-ttu-id="9e66a-435">[[:space:]]</span><span class="sxs-lookup"><span data-stu-id="9e66a-435">[[:space:]]</span></span> | <span data-ttu-id="9e66a-436">空格 (≡ [\t\n\v\f\r])</span><span class="sxs-lookup"><span data-stu-id="9e66a-436">whitespace (≡ [\t\n\v\f\r])</span></span> |
| <span data-ttu-id="9e66a-437">[[:upper:]]</span><span class="sxs-lookup"><span data-stu-id="9e66a-437">[[:upper:]]</span></span> | <span data-ttu-id="9e66a-438">大寫 (≡ [A-Z])</span><span class="sxs-lookup"><span data-stu-id="9e66a-438">upper case (≡ [A-Z])</span></span> |
| <span data-ttu-id="9e66a-439">[[:word:]]</span><span class="sxs-lookup"><span data-stu-id="9e66a-439">[[:word:]]</span></span> | <span data-ttu-id="9e66a-440">文字字元 (≡ [0-9A-Za-z\_])</span><span class="sxs-lookup"><span data-stu-id="9e66a-440">word characters (≡ [0-9A-Za-z\_])</span></span> |
| <span data-ttu-id="9e66a-441">[[:xdigit:]]</span><span class="sxs-lookup"><span data-stu-id="9e66a-441">[[:xdigit:]]</span></span> | <span data-ttu-id="9e66a-442">十六進位數位 (≡ [0-9A-Fa-f])</span><span class="sxs-lookup"><span data-stu-id="9e66a-442">hex digit (≡ [0-9A-Fa-f])</span></span> |

| | <span data-ttu-id="9e66a-443">Unicode 字元類名 --一般類別</span><span class="sxs-lookup"><span data-stu-id="9e66a-443">Unicode character class names--general category</span></span> |
| --- | --- |
| <span data-ttu-id="9e66a-444">C</span><span class="sxs-lookup"><span data-stu-id="9e66a-444">C</span></span> | <span data-ttu-id="9e66a-445">其他</span><span class="sxs-lookup"><span data-stu-id="9e66a-445">other</span></span> |
| <span data-ttu-id="9e66a-446">副本</span><span class="sxs-lookup"><span data-stu-id="9e66a-446">Cc</span></span> | <span data-ttu-id="9e66a-447">control</span><span class="sxs-lookup"><span data-stu-id="9e66a-447">control</span></span> |
| <span data-ttu-id="9e66a-448">Cf</span><span class="sxs-lookup"><span data-stu-id="9e66a-448">Cf</span></span> | <span data-ttu-id="9e66a-449">format</span><span class="sxs-lookup"><span data-stu-id="9e66a-449">format</span></span> |
| <span data-ttu-id="9e66a-450">Cn</span><span class="sxs-lookup"><span data-stu-id="9e66a-450">Cn</span></span> | <span data-ttu-id="9e66a-451">未指派的代碼點 (不支援)</span><span class="sxs-lookup"><span data-stu-id="9e66a-451">unassigned code points (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="9e66a-452">Co</span><span class="sxs-lookup"><span data-stu-id="9e66a-452">Co</span></span> | <span data-ttu-id="9e66a-453">私密用法</span><span class="sxs-lookup"><span data-stu-id="9e66a-453">private use</span></span> |
| <span data-ttu-id="9e66a-454">Cs</span><span class="sxs-lookup"><span data-stu-id="9e66a-454">Cs</span></span> | <span data-ttu-id="9e66a-455">替代</span><span class="sxs-lookup"><span data-stu-id="9e66a-455">surrogate</span></span> |
| <span data-ttu-id="9e66a-456">L</span><span class="sxs-lookup"><span data-stu-id="9e66a-456">L</span></span> | <span data-ttu-id="9e66a-457">字母</span><span class="sxs-lookup"><span data-stu-id="9e66a-457">letter</span></span> |
| <span data-ttu-id="9e66a-458">LC</span><span class="sxs-lookup"><span data-stu-id="9e66a-458">LC</span></span> | <span data-ttu-id="9e66a-459">大小寫字母 (不支援)</span><span class="sxs-lookup"><span data-stu-id="9e66a-459">cased letter (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="9e66a-460">L&amp;</span><span class="sxs-lookup"><span data-stu-id="9e66a-460">L&amp;</span></span> | <span data-ttu-id="9e66a-461">大小寫字母 (不支援)</span><span class="sxs-lookup"><span data-stu-id="9e66a-461">cased letter (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="9e66a-462">Ll</span><span class="sxs-lookup"><span data-stu-id="9e66a-462">Ll</span></span> | <span data-ttu-id="9e66a-463">小寫字母</span><span class="sxs-lookup"><span data-stu-id="9e66a-463">lowercase letter</span></span> |
| <span data-ttu-id="9e66a-464">Lm</span><span class="sxs-lookup"><span data-stu-id="9e66a-464">Lm</span></span> | <span data-ttu-id="9e66a-465">修飾詞字母</span><span class="sxs-lookup"><span data-stu-id="9e66a-465">modifier letter</span></span> |
| <span data-ttu-id="9e66a-466">Lo</span><span class="sxs-lookup"><span data-stu-id="9e66a-466">Lo</span></span> | <span data-ttu-id="9e66a-467">其他字母</span><span class="sxs-lookup"><span data-stu-id="9e66a-467">other letter</span></span> |
| <span data-ttu-id="9e66a-468">Lt</span><span class="sxs-lookup"><span data-stu-id="9e66a-468">Lt</span></span> | <span data-ttu-id="9e66a-469">大寫字母</span><span class="sxs-lookup"><span data-stu-id="9e66a-469">titlecase letter</span></span> |
| <span data-ttu-id="9e66a-470">Lu</span><span class="sxs-lookup"><span data-stu-id="9e66a-470">Lu</span></span> | <span data-ttu-id="9e66a-471">大寫字母</span><span class="sxs-lookup"><span data-stu-id="9e66a-471">uppercase letter</span></span> |
| <span data-ttu-id="9e66a-472">M</span><span class="sxs-lookup"><span data-stu-id="9e66a-472">M</span></span> | <span data-ttu-id="9e66a-473">標記</span><span class="sxs-lookup"><span data-stu-id="9e66a-473">mark</span></span> |
| <span data-ttu-id="9e66a-474">Mc</span><span class="sxs-lookup"><span data-stu-id="9e66a-474">Mc</span></span> | <span data-ttu-id="9e66a-475">間距標記</span><span class="sxs-lookup"><span data-stu-id="9e66a-475">spacing mark</span></span> |
| <span data-ttu-id="9e66a-476">Me</span><span class="sxs-lookup"><span data-stu-id="9e66a-476">Me</span></span> | <span data-ttu-id="9e66a-477">封閉標記</span><span class="sxs-lookup"><span data-stu-id="9e66a-477">enclosing mark</span></span> |
| <span data-ttu-id="9e66a-478">Mn</span><span class="sxs-lookup"><span data-stu-id="9e66a-478">Mn</span></span> | <span data-ttu-id="9e66a-479">非間距標記</span><span class="sxs-lookup"><span data-stu-id="9e66a-479">non-spacing mark</span></span> |
| <span data-ttu-id="9e66a-480">N</span><span class="sxs-lookup"><span data-stu-id="9e66a-480">N</span></span> | <span data-ttu-id="9e66a-481">數字</span><span class="sxs-lookup"><span data-stu-id="9e66a-481">number</span></span> |
| <span data-ttu-id="9e66a-482">Nd</span><span class="sxs-lookup"><span data-stu-id="9e66a-482">Nd</span></span> | <span data-ttu-id="9e66a-483">十進位數</span><span class="sxs-lookup"><span data-stu-id="9e66a-483">decimal number</span></span> |
| <span data-ttu-id="9e66a-484">Nl</span><span class="sxs-lookup"><span data-stu-id="9e66a-484">Nl</span></span> | <span data-ttu-id="9e66a-485">字母數字</span><span class="sxs-lookup"><span data-stu-id="9e66a-485">letter number</span></span> |
| <span data-ttu-id="9e66a-486">否</span><span class="sxs-lookup"><span data-stu-id="9e66a-486">No</span></span> | <span data-ttu-id="9e66a-487">其他數字</span><span class="sxs-lookup"><span data-stu-id="9e66a-487">other number</span></span> |
| <span data-ttu-id="9e66a-488">P</span><span class="sxs-lookup"><span data-stu-id="9e66a-488">P</span></span> | <span data-ttu-id="9e66a-489">標點符號</span><span class="sxs-lookup"><span data-stu-id="9e66a-489">punctuation</span></span> |
| <span data-ttu-id="9e66a-490">Pc</span><span class="sxs-lookup"><span data-stu-id="9e66a-490">Pc</span></span> | <span data-ttu-id="9e66a-491">連接器標點符號</span><span class="sxs-lookup"><span data-stu-id="9e66a-491">connector punctuation</span></span> |
| <span data-ttu-id="9e66a-492">Pd</span><span class="sxs-lookup"><span data-stu-id="9e66a-492">Pd</span></span> | <span data-ttu-id="9e66a-493">虛線標點符號</span><span class="sxs-lookup"><span data-stu-id="9e66a-493">dash punctuation</span></span> |
| <span data-ttu-id="9e66a-494">Pe</span><span class="sxs-lookup"><span data-stu-id="9e66a-494">Pe</span></span> | <span data-ttu-id="9e66a-495">關閉標點符號</span><span class="sxs-lookup"><span data-stu-id="9e66a-495">close punctuation</span></span> |
| <span data-ttu-id="9e66a-496">Pf</span><span class="sxs-lookup"><span data-stu-id="9e66a-496">Pf</span></span> | <span data-ttu-id="9e66a-497">末位標點符號</span><span class="sxs-lookup"><span data-stu-id="9e66a-497">final punctuation</span></span> |
| <span data-ttu-id="9e66a-498">Pi</span><span class="sxs-lookup"><span data-stu-id="9e66a-498">Pi</span></span> | <span data-ttu-id="9e66a-499">首位標點</span><span class="sxs-lookup"><span data-stu-id="9e66a-499">initial punctuation</span></span> |
| <span data-ttu-id="9e66a-500">Po</span><span class="sxs-lookup"><span data-stu-id="9e66a-500">Po</span></span> | <span data-ttu-id="9e66a-501">其他標點符號</span><span class="sxs-lookup"><span data-stu-id="9e66a-501">other punctuation</span></span> |
| <span data-ttu-id="9e66a-502">Ps</span><span class="sxs-lookup"><span data-stu-id="9e66a-502">Ps</span></span> | <span data-ttu-id="9e66a-503">開放標點符號</span><span class="sxs-lookup"><span data-stu-id="9e66a-503">open punctuation</span></span> |
| <span data-ttu-id="9e66a-504">S</span><span class="sxs-lookup"><span data-stu-id="9e66a-504">S</span></span> | <span data-ttu-id="9e66a-505">symbol</span><span class="sxs-lookup"><span data-stu-id="9e66a-505">symbol</span></span> |
| <span data-ttu-id="9e66a-506">Sc</span><span class="sxs-lookup"><span data-stu-id="9e66a-506">Sc</span></span> | <span data-ttu-id="9e66a-507">貨幣符號</span><span class="sxs-lookup"><span data-stu-id="9e66a-507">currency symbol</span></span> |
| <span data-ttu-id="9e66a-508">Sk</span><span class="sxs-lookup"><span data-stu-id="9e66a-508">Sk</span></span> | <span data-ttu-id="9e66a-509">修飾詞符號</span><span class="sxs-lookup"><span data-stu-id="9e66a-509">modifier symbol</span></span> |
| <span data-ttu-id="9e66a-510">Sm</span><span class="sxs-lookup"><span data-stu-id="9e66a-510">Sm</span></span> | <span data-ttu-id="9e66a-511">數學符號</span><span class="sxs-lookup"><span data-stu-id="9e66a-511">math symbol</span></span> |
| <span data-ttu-id="9e66a-512">So</span><span class="sxs-lookup"><span data-stu-id="9e66a-512">So</span></span> | <span data-ttu-id="9e66a-513">其他符號</span><span class="sxs-lookup"><span data-stu-id="9e66a-513">other symbol</span></span> |
| <span data-ttu-id="9e66a-514">Z</span><span class="sxs-lookup"><span data-stu-id="9e66a-514">Z</span></span> | <span data-ttu-id="9e66a-515">分隔符號</span><span class="sxs-lookup"><span data-stu-id="9e66a-515">separator</span></span> |
| <span data-ttu-id="9e66a-516">Zl</span><span class="sxs-lookup"><span data-stu-id="9e66a-516">Zl</span></span> | <span data-ttu-id="9e66a-517">行分隔符號</span><span class="sxs-lookup"><span data-stu-id="9e66a-517">line separator</span></span> |
| <span data-ttu-id="9e66a-518">Zp</span><span class="sxs-lookup"><span data-stu-id="9e66a-518">Zp</span></span> | <span data-ttu-id="9e66a-519">段落分隔符號</span><span class="sxs-lookup"><span data-stu-id="9e66a-519">paragraph separator</span></span> |
| <span data-ttu-id="9e66a-520">Zs</span><span class="sxs-lookup"><span data-stu-id="9e66a-520">Zs</span></span> | <span data-ttu-id="9e66a-521">空格分隔符號</span><span class="sxs-lookup"><span data-stu-id="9e66a-521">space separator</span></span> |

| <span data-ttu-id="9e66a-522">Unicode 字元類名 -- 指令碼</span><span class="sxs-lookup"><span data-stu-id="9e66a-522">Unicode character class names--scripts</span></span> |
| --- |
| <span data-ttu-id="9e66a-523">Adlam 文</span><span class="sxs-lookup"><span data-stu-id="9e66a-523">Adlam</span></span> |
| <span data-ttu-id="9e66a-524">阿洪姆語</span><span class="sxs-lookup"><span data-stu-id="9e66a-524">Ahom</span></span> |
| <span data-ttu-id="9e66a-525">Anatolian\_Hieroglyphs</span><span class="sxs-lookup"><span data-stu-id="9e66a-525">Anatolian\_Hieroglyphs</span></span> |
| <span data-ttu-id="9e66a-526">阿拉伯文</span><span class="sxs-lookup"><span data-stu-id="9e66a-526">Arabic</span></span> |
| <span data-ttu-id="9e66a-527">亞美尼亞文</span><span class="sxs-lookup"><span data-stu-id="9e66a-527">Armenian</span></span> |
| <span data-ttu-id="9e66a-528">阿維斯塔文</span><span class="sxs-lookup"><span data-stu-id="9e66a-528">Avestan</span></span> |
| <span data-ttu-id="9e66a-529">峇里文</span><span class="sxs-lookup"><span data-stu-id="9e66a-529">Balinese</span></span> |
| <span data-ttu-id="9e66a-530">巴姆文</span><span class="sxs-lookup"><span data-stu-id="9e66a-530">Bamum</span></span> |
| <span data-ttu-id="9e66a-531">Bassa\_Vah</span><span class="sxs-lookup"><span data-stu-id="9e66a-531">Bassa\_Vah</span></span> |
| <span data-ttu-id="9e66a-532">巴塔克文</span><span class="sxs-lookup"><span data-stu-id="9e66a-532">Batak</span></span> |
| <span data-ttu-id="9e66a-533">孟加拉文</span><span class="sxs-lookup"><span data-stu-id="9e66a-533">Bengali</span></span> |
| <span data-ttu-id="9e66a-534">拜克舒基文</span><span class="sxs-lookup"><span data-stu-id="9e66a-534">Bhaiksuki</span></span> |
| <span data-ttu-id="9e66a-535">注音符號</span><span class="sxs-lookup"><span data-stu-id="9e66a-535">Bopomofo</span></span> |
| <span data-ttu-id="9e66a-536">婆羅米文</span><span class="sxs-lookup"><span data-stu-id="9e66a-536">Brahmi</span></span> |
| <span data-ttu-id="9e66a-537">點字</span><span class="sxs-lookup"><span data-stu-id="9e66a-537">Braille</span></span> |
| <span data-ttu-id="9e66a-538">布吉斯文</span><span class="sxs-lookup"><span data-stu-id="9e66a-538">Buginese</span></span> |
| <span data-ttu-id="9e66a-539">布錫語</span><span class="sxs-lookup"><span data-stu-id="9e66a-539">Buhid</span></span> |
| <span data-ttu-id="9e66a-540">Canadian\_Aboriginal</span><span class="sxs-lookup"><span data-stu-id="9e66a-540">Canadian\_Aboriginal</span></span> |
| <span data-ttu-id="9e66a-541">卡里亞文</span><span class="sxs-lookup"><span data-stu-id="9e66a-541">Carian</span></span> |
| <span data-ttu-id="9e66a-542">Caucasian\_Albanian</span><span class="sxs-lookup"><span data-stu-id="9e66a-542">Caucasian\_Albanian</span></span> |
| <span data-ttu-id="9e66a-543">查克馬文</span><span class="sxs-lookup"><span data-stu-id="9e66a-543">Chakma</span></span> |
| <span data-ttu-id="9e66a-544">Cham</span><span class="sxs-lookup"><span data-stu-id="9e66a-544">Cham</span></span> |
| <span data-ttu-id="9e66a-545">卻洛奇文</span><span class="sxs-lookup"><span data-stu-id="9e66a-545">Cherokee</span></span> |
| <span data-ttu-id="9e66a-546">花剌子模語</span><span class="sxs-lookup"><span data-stu-id="9e66a-546">Chorasmian</span></span> |
| <span data-ttu-id="9e66a-547">通用</span><span class="sxs-lookup"><span data-stu-id="9e66a-547">Common</span></span> |
| <span data-ttu-id="9e66a-548">科普特語</span><span class="sxs-lookup"><span data-stu-id="9e66a-548">Coptic</span></span> |
| <span data-ttu-id="9e66a-549">楔形文字</span><span class="sxs-lookup"><span data-stu-id="9e66a-549">Cuneiform</span></span> |
| <span data-ttu-id="9e66a-550">賽普勒斯</span><span class="sxs-lookup"><span data-stu-id="9e66a-550">Cypriot</span></span> |
| <span data-ttu-id="9e66a-551">西里爾文</span><span class="sxs-lookup"><span data-stu-id="9e66a-551">Cyrillic</span></span> |
| <span data-ttu-id="9e66a-552">德瑟列特文</span><span class="sxs-lookup"><span data-stu-id="9e66a-552">Deseret</span></span> |
| <span data-ttu-id="9e66a-553">梵文字母</span><span class="sxs-lookup"><span data-stu-id="9e66a-553">Devanagari</span></span> |
| <span data-ttu-id="9e66a-554">Dives\_Akuru</span><span class="sxs-lookup"><span data-stu-id="9e66a-554">Dives\_Akuru</span></span> |
| <span data-ttu-id="9e66a-555">Dogra 文</span><span class="sxs-lookup"><span data-stu-id="9e66a-555">Dogra</span></span> |
| <span data-ttu-id="9e66a-556">杜普雷速记</span><span class="sxs-lookup"><span data-stu-id="9e66a-556">Duployan</span></span> |
| <span data-ttu-id="9e66a-557">Egyptian\_Hieroglyphs</span><span class="sxs-lookup"><span data-stu-id="9e66a-557">Egyptian\_Hieroglyphs</span></span> |
| <span data-ttu-id="9e66a-558">艾巴申語</span><span class="sxs-lookup"><span data-stu-id="9e66a-558">Elbasan</span></span> |
| <span data-ttu-id="9e66a-559">埃利邁文</span><span class="sxs-lookup"><span data-stu-id="9e66a-559">Elymaic</span></span> |
| <span data-ttu-id="9e66a-560">衣索比亞文</span><span class="sxs-lookup"><span data-stu-id="9e66a-560">Ethiopic</span></span> |
| <span data-ttu-id="9e66a-561">喬治亞文</span><span class="sxs-lookup"><span data-stu-id="9e66a-561">Georgian</span></span> |
| <span data-ttu-id="9e66a-562">格來哥利蒂克文</span><span class="sxs-lookup"><span data-stu-id="9e66a-562">Glagolitic</span></span> |
| <span data-ttu-id="9e66a-563">歌德</span><span class="sxs-lookup"><span data-stu-id="9e66a-563">Gothic</span></span> |
| <span data-ttu-id="9e66a-564">古蘭塔文</span><span class="sxs-lookup"><span data-stu-id="9e66a-564">Grantha</span></span> |
| <span data-ttu-id="9e66a-565">希臘文</span><span class="sxs-lookup"><span data-stu-id="9e66a-565">Greek</span></span> |
| <span data-ttu-id="9e66a-566">古吉拉特文</span><span class="sxs-lookup"><span data-stu-id="9e66a-566">Gujarati</span></span> |
| <span data-ttu-id="9e66a-567">Gunjala\_Gondi</span><span class="sxs-lookup"><span data-stu-id="9e66a-567">Gunjala\_Gondi</span></span> |
| <span data-ttu-id="9e66a-568">果魯穆奇文字</span><span class="sxs-lookup"><span data-stu-id="9e66a-568">Gurmukhi</span></span> |
| <span data-ttu-id="9e66a-569">漢語</span><span class="sxs-lookup"><span data-stu-id="9e66a-569">Han</span></span> |
| <span data-ttu-id="9e66a-570">諺文</span><span class="sxs-lookup"><span data-stu-id="9e66a-570">Hangul</span></span> |
| <span data-ttu-id="9e66a-571">Hanifi\_Rohingya</span><span class="sxs-lookup"><span data-stu-id="9e66a-571">Hanifi\_Rohingya</span></span> |
| <span data-ttu-id="9e66a-572">漢奴勞族文</span><span class="sxs-lookup"><span data-stu-id="9e66a-572">Hanunoo</span></span> |
| <span data-ttu-id="9e66a-573">哈特拉文</span><span class="sxs-lookup"><span data-stu-id="9e66a-573">Hatran</span></span> |
| <span data-ttu-id="9e66a-574">希伯來文</span><span class="sxs-lookup"><span data-stu-id="9e66a-574">Hebrew</span></span> |
| <span data-ttu-id="9e66a-575">平假名</span><span class="sxs-lookup"><span data-stu-id="9e66a-575">Hiragana</span></span> |
| <span data-ttu-id="9e66a-576">Imperial\_Aramaic</span><span class="sxs-lookup"><span data-stu-id="9e66a-576">Imperial\_Aramaic</span></span> |
| <span data-ttu-id="9e66a-577">已繼承</span><span class="sxs-lookup"><span data-stu-id="9e66a-577">Inherited</span></span> |
| <span data-ttu-id="9e66a-578">Inscriptional\_Pahlavi</span><span class="sxs-lookup"><span data-stu-id="9e66a-578">Inscriptional\_Pahlavi</span></span> |
| <span data-ttu-id="9e66a-579">Inscriptional\_Parthian</span><span class="sxs-lookup"><span data-stu-id="9e66a-579">Inscriptional\_Parthian</span></span> |
| <span data-ttu-id="9e66a-580">爪哇文</span><span class="sxs-lookup"><span data-stu-id="9e66a-580">Javanese</span></span> |
| <span data-ttu-id="9e66a-581">凱提體文</span><span class="sxs-lookup"><span data-stu-id="9e66a-581">Kaithi</span></span> |
| <span data-ttu-id="9e66a-582">坎那達文</span><span class="sxs-lookup"><span data-stu-id="9e66a-582">Kannada</span></span> |
| <span data-ttu-id="9e66a-583">片假名</span><span class="sxs-lookup"><span data-stu-id="9e66a-583">Katakana</span></span> |
| <span data-ttu-id="9e66a-584">Kayah\_Li</span><span class="sxs-lookup"><span data-stu-id="9e66a-584">Kayah\_Li</span></span> |
| <span data-ttu-id="9e66a-585">佉盧文</span><span class="sxs-lookup"><span data-stu-id="9e66a-585">Kharoshthi</span></span> |
| <span data-ttu-id="9e66a-586">Khitan\_Small\_Script</span><span class="sxs-lookup"><span data-stu-id="9e66a-586">Khitan\_Small\_Script</span></span> |
| <span data-ttu-id="9e66a-587">高棉文</span><span class="sxs-lookup"><span data-stu-id="9e66a-587">Khmer</span></span> |
| <span data-ttu-id="9e66a-588">郝吉文</span><span class="sxs-lookup"><span data-stu-id="9e66a-588">Khojki</span></span> |
| <span data-ttu-id="9e66a-589">信德文</span><span class="sxs-lookup"><span data-stu-id="9e66a-589">Khudawadi</span></span> |
| <span data-ttu-id="9e66a-590">寮文</span><span class="sxs-lookup"><span data-stu-id="9e66a-590">Lao</span></span> |
| <span data-ttu-id="9e66a-591">拉丁文</span><span class="sxs-lookup"><span data-stu-id="9e66a-591">Latin</span></span> |
| <span data-ttu-id="9e66a-592">雷布查文</span><span class="sxs-lookup"><span data-stu-id="9e66a-592">Lepcha</span></span> |
| <span data-ttu-id="9e66a-593">林布文</span><span class="sxs-lookup"><span data-stu-id="9e66a-593">Limbu</span></span> |
| <span data-ttu-id="9e66a-594">Linear\_A</span><span class="sxs-lookup"><span data-stu-id="9e66a-594">Linear\_A</span></span> |
| <span data-ttu-id="9e66a-595">Linear\_B</span><span class="sxs-lookup"><span data-stu-id="9e66a-595">Linear\_B</span></span> |
| <span data-ttu-id="9e66a-596">栗粟文</span><span class="sxs-lookup"><span data-stu-id="9e66a-596">Lisu</span></span> |
| <span data-ttu-id="9e66a-597">呂西亞文</span><span class="sxs-lookup"><span data-stu-id="9e66a-597">Lycian</span></span> |
| <span data-ttu-id="9e66a-598">利底亞文</span><span class="sxs-lookup"><span data-stu-id="9e66a-598">Lydian</span></span> |
| <span data-ttu-id="9e66a-599">馬哈加尼文</span><span class="sxs-lookup"><span data-stu-id="9e66a-599">Mahajani</span></span> |
| <span data-ttu-id="9e66a-600">瑪加沙文</span><span class="sxs-lookup"><span data-stu-id="9e66a-600">Makasar</span></span> |
| <span data-ttu-id="9e66a-601">馬來亞拉姆文</span><span class="sxs-lookup"><span data-stu-id="9e66a-601">Malayalam</span></span> |
| <span data-ttu-id="9e66a-602">曼底克文</span><span class="sxs-lookup"><span data-stu-id="9e66a-602">Mandaic</span></span> |
| <span data-ttu-id="9e66a-603">摩尼文</span><span class="sxs-lookup"><span data-stu-id="9e66a-603">Manichaean</span></span> |
| <span data-ttu-id="9e66a-604">Marchen 文</span><span class="sxs-lookup"><span data-stu-id="9e66a-604">Marchen</span></span> |
| <span data-ttu-id="9e66a-605">Masaram\_Gondi</span><span class="sxs-lookup"><span data-stu-id="9e66a-605">Masaram\_Gondi</span></span> |
| <span data-ttu-id="9e66a-606">梅德法伊德林文</span><span class="sxs-lookup"><span data-stu-id="9e66a-606">Medefaidrin</span></span> |
| <span data-ttu-id="9e66a-607">Meetei\_Mayek</span><span class="sxs-lookup"><span data-stu-id="9e66a-607">Meetei\_Mayek</span></span> |
| <span data-ttu-id="9e66a-608">Mende\_Kikakui</span><span class="sxs-lookup"><span data-stu-id="9e66a-608">Mende\_Kikakui</span></span> |
| <span data-ttu-id="9e66a-609">Meroitic\_Cursive</span><span class="sxs-lookup"><span data-stu-id="9e66a-609">Meroitic\_Cursive</span></span> |
| <span data-ttu-id="9e66a-610">Meroitic\_Hieroglyphs</span><span class="sxs-lookup"><span data-stu-id="9e66a-610">Meroitic\_Hieroglyphs</span></span> |
| <span data-ttu-id="9e66a-611">苗文</span><span class="sxs-lookup"><span data-stu-id="9e66a-611">Miao</span></span> |
| <span data-ttu-id="9e66a-612">Modi 文</span><span class="sxs-lookup"><span data-stu-id="9e66a-612">Modi</span></span> |
| <span data-ttu-id="9e66a-613">蒙古文</span><span class="sxs-lookup"><span data-stu-id="9e66a-613">Mongolian</span></span> |
| <span data-ttu-id="9e66a-614">姆諾文</span><span class="sxs-lookup"><span data-stu-id="9e66a-614">Mro</span></span> |
| <span data-ttu-id="9e66a-615">Multani 文</span><span class="sxs-lookup"><span data-stu-id="9e66a-615">Multani</span></span> |
| <span data-ttu-id="9e66a-616">緬甸</span><span class="sxs-lookup"><span data-stu-id="9e66a-616">Myanmar</span></span> |
| <span data-ttu-id="9e66a-617">納巴泰文</span><span class="sxs-lookup"><span data-stu-id="9e66a-617">Nabataean</span></span> |
| <span data-ttu-id="9e66a-618">南迪城文</span><span class="sxs-lookup"><span data-stu-id="9e66a-618">Nandinagari</span></span> |
| <span data-ttu-id="9e66a-619">New\_Tai\_Lue</span><span class="sxs-lookup"><span data-stu-id="9e66a-619">New\_Tai\_Lue</span></span> |
| <span data-ttu-id="9e66a-620">Newa 文</span><span class="sxs-lookup"><span data-stu-id="9e66a-620">Newa</span></span> |
| <span data-ttu-id="9e66a-621">西非書面文字</span><span class="sxs-lookup"><span data-stu-id="9e66a-621">Nko</span></span> |
| <span data-ttu-id="9e66a-622">女書</span><span class="sxs-lookup"><span data-stu-id="9e66a-622">Nushu</span></span> |
| <span data-ttu-id="9e66a-623">Nyiakeng\_Puachue\_Hmong</span><span class="sxs-lookup"><span data-stu-id="9e66a-623">Nyiakeng\_Puachue\_Hmong</span></span> |
| <span data-ttu-id="9e66a-624">歐甘字母</span><span class="sxs-lookup"><span data-stu-id="9e66a-624">Ogham</span></span> |
| <span data-ttu-id="9e66a-625">Ol\_Chiki</span><span class="sxs-lookup"><span data-stu-id="9e66a-625">Ol\_Chiki</span></span> |
| <span data-ttu-id="9e66a-626">Old\_Hungarian</span><span class="sxs-lookup"><span data-stu-id="9e66a-626">Old\_Hungarian</span></span> |
| <span data-ttu-id="9e66a-627">Old\_Italic</span><span class="sxs-lookup"><span data-stu-id="9e66a-627">Old\_Italic</span></span> |
| <span data-ttu-id="9e66a-628">Old\_North\_Arabian</span><span class="sxs-lookup"><span data-stu-id="9e66a-628">Old\_North\_Arabian</span></span> |
| <span data-ttu-id="9e66a-629">Old\_Permic</span><span class="sxs-lookup"><span data-stu-id="9e66a-629">Old\_Permic</span></span> |
| <span data-ttu-id="9e66a-630">Old\_Persian</span><span class="sxs-lookup"><span data-stu-id="9e66a-630">Old\_Persian</span></span> |
| <span data-ttu-id="9e66a-631">Old\_Sogdian</span><span class="sxs-lookup"><span data-stu-id="9e66a-631">Old\_Sogdian</span></span> |
| <span data-ttu-id="9e66a-632">Old\_South\_Arabian</span><span class="sxs-lookup"><span data-stu-id="9e66a-632">Old\_South\_Arabian</span></span> |
| <span data-ttu-id="9e66a-633">Old\_Turkic</span><span class="sxs-lookup"><span data-stu-id="9e66a-633">Old\_Turkic</span></span> |
| <span data-ttu-id="9e66a-634">奧里亞語</span><span class="sxs-lookup"><span data-stu-id="9e66a-634">Oriya</span></span> |
| <span data-ttu-id="9e66a-635">奧賽治文</span><span class="sxs-lookup"><span data-stu-id="9e66a-635">Osage</span></span> |
| <span data-ttu-id="9e66a-636">奧斯曼亞文</span><span class="sxs-lookup"><span data-stu-id="9e66a-636">Osmanya</span></span> |
| <span data-ttu-id="9e66a-637">Pahawh\_Hmong</span><span class="sxs-lookup"><span data-stu-id="9e66a-637">Pahawh\_Hmong</span></span> |
| <span data-ttu-id="9e66a-638">帕爾邁拉文</span><span class="sxs-lookup"><span data-stu-id="9e66a-638">Palmyrene</span></span> |
| <span data-ttu-id="9e66a-639">Pau\_Cin\_Hau</span><span class="sxs-lookup"><span data-stu-id="9e66a-639">Pau\_Cin\_Hau</span></span> |
| <span data-ttu-id="9e66a-640">Phags\_Pa</span><span class="sxs-lookup"><span data-stu-id="9e66a-640">Phags\_Pa</span></span> |
| <span data-ttu-id="9e66a-641">腓尼基文</span><span class="sxs-lookup"><span data-stu-id="9e66a-641">Phoenician</span></span> |
| <span data-ttu-id="9e66a-642">Psalter\_Pahlavi</span><span class="sxs-lookup"><span data-stu-id="9e66a-642">Psalter\_Pahlavi</span></span> |
| <span data-ttu-id="9e66a-643">拉讓文</span><span class="sxs-lookup"><span data-stu-id="9e66a-643">Rejang</span></span> |
| <span data-ttu-id="9e66a-644">盧恩文</span><span class="sxs-lookup"><span data-stu-id="9e66a-644">Runic</span></span> |
| <span data-ttu-id="9e66a-645">撒馬利亞文</span><span class="sxs-lookup"><span data-stu-id="9e66a-645">Samaritan</span></span> |
| <span data-ttu-id="9e66a-646">紹拉斯徹文</span><span class="sxs-lookup"><span data-stu-id="9e66a-646">Saurashtra</span></span> |
| <span data-ttu-id="9e66a-647">沙拉達文</span><span class="sxs-lookup"><span data-stu-id="9e66a-647">Sharada</span></span> |
| <span data-ttu-id="9e66a-648">蕭伯納文</span><span class="sxs-lookup"><span data-stu-id="9e66a-648">Shavian</span></span> |
| <span data-ttu-id="9e66a-649">悉曇文</span><span class="sxs-lookup"><span data-stu-id="9e66a-649">Siddham</span></span> |
| <span data-ttu-id="9e66a-650">手語書寫</span><span class="sxs-lookup"><span data-stu-id="9e66a-650">SignWriting</span></span> |
| <span data-ttu-id="9e66a-651">僧伽羅文</span><span class="sxs-lookup"><span data-stu-id="9e66a-651">Sinhala</span></span> |
| <span data-ttu-id="9e66a-652">粟特文</span><span class="sxs-lookup"><span data-stu-id="9e66a-652">Sogdian</span></span> |
| <span data-ttu-id="9e66a-653">Sora\_Sompeng</span><span class="sxs-lookup"><span data-stu-id="9e66a-653">Sora\_Sompeng</span></span> |
| <span data-ttu-id="9e66a-654">索永布文</span><span class="sxs-lookup"><span data-stu-id="9e66a-654">Soyombo</span></span> |
| <span data-ttu-id="9e66a-655">巽丹文</span><span class="sxs-lookup"><span data-stu-id="9e66a-655">Sundanese</span></span> |
| <span data-ttu-id="9e66a-656">Syloti\_Nagri</span><span class="sxs-lookup"><span data-stu-id="9e66a-656">Syloti\_Nagri</span></span> |
| <span data-ttu-id="9e66a-657">敘利亞文</span><span class="sxs-lookup"><span data-stu-id="9e66a-657">Syriac</span></span> |
| <span data-ttu-id="9e66a-658">他加祿語</span><span class="sxs-lookup"><span data-stu-id="9e66a-658">Tagalog</span></span> |
| <span data-ttu-id="9e66a-659">塔班瓦語</span><span class="sxs-lookup"><span data-stu-id="9e66a-659">Tagbanwa</span></span> |
| <span data-ttu-id="9e66a-660">Tai\_Le</span><span class="sxs-lookup"><span data-stu-id="9e66a-660">Tai\_Le</span></span> |
| <span data-ttu-id="9e66a-661">Tai\_Tham</span><span class="sxs-lookup"><span data-stu-id="9e66a-661">Tai\_Tham</span></span> |
| <span data-ttu-id="9e66a-662">Tai\_Viet</span><span class="sxs-lookup"><span data-stu-id="9e66a-662">Tai\_Viet</span></span> |
| <span data-ttu-id="9e66a-663">塔卡里文</span><span class="sxs-lookup"><span data-stu-id="9e66a-663">Takri</span></span> |
| <span data-ttu-id="9e66a-664">坦米爾文</span><span class="sxs-lookup"><span data-stu-id="9e66a-664">Tamil</span></span> |
| <span data-ttu-id="9e66a-665">西夏語</span><span class="sxs-lookup"><span data-stu-id="9e66a-665">Tangut</span></span> |
| <span data-ttu-id="9e66a-666">特拉古文</span><span class="sxs-lookup"><span data-stu-id="9e66a-666">Telugu</span></span> |
| <span data-ttu-id="9e66a-667">塔安那文</span><span class="sxs-lookup"><span data-stu-id="9e66a-667">Thaana</span></span> |
| <span data-ttu-id="9e66a-668">泰文</span><span class="sxs-lookup"><span data-stu-id="9e66a-668">Thai</span></span> |
| <span data-ttu-id="9e66a-669">藏文</span><span class="sxs-lookup"><span data-stu-id="9e66a-669">Tibetan</span></span> |
| <span data-ttu-id="9e66a-670">提弗納文</span><span class="sxs-lookup"><span data-stu-id="9e66a-670">Tifinagh</span></span> |
| <span data-ttu-id="9e66a-671">底羅仆多文</span><span class="sxs-lookup"><span data-stu-id="9e66a-671">Tirhuta</span></span> |
| <span data-ttu-id="9e66a-672">烏加里特語</span><span class="sxs-lookup"><span data-stu-id="9e66a-672">Ugaritic</span></span> |
| <span data-ttu-id="9e66a-673">范文</span><span class="sxs-lookup"><span data-stu-id="9e66a-673">Vai</span></span> |
| <span data-ttu-id="9e66a-674">Wancho 語</span><span class="sxs-lookup"><span data-stu-id="9e66a-674">Wancho</span></span> |
| <span data-ttu-id="9e66a-675">Warang\_Citi</span><span class="sxs-lookup"><span data-stu-id="9e66a-675">Warang\_Citi</span></span> |
| <span data-ttu-id="9e66a-676">亞茲迪文</span><span class="sxs-lookup"><span data-stu-id="9e66a-676">Yezidi</span></span> |
| <span data-ttu-id="9e66a-677">彝文</span><span class="sxs-lookup"><span data-stu-id="9e66a-677">Yi</span></span> |
| <span data-ttu-id="9e66a-678">Zanabazar\_Square</span><span class="sxs-lookup"><span data-stu-id="9e66a-678">Zanabazar\_Square</span></span> |

|  | <span data-ttu-id="9e66a-679">Vim 字元類別</span><span class="sxs-lookup"><span data-stu-id="9e66a-679">Vim character classes</span></span> |
| --- | --- |
| <span data-ttu-id="9e66a-680">\i</span><span class="sxs-lookup"><span data-stu-id="9e66a-680">\i</span></span> | <span data-ttu-id="9e66a-681">識別碼字元 FF (不支援) VIM</span><span class="sxs-lookup"><span data-stu-id="9e66a-681">identifier character (NOT SUPPORTED) VIM</span></span> |
| <span data-ttu-id="9e66a-682">\I</span><span class="sxs-lookup"><span data-stu-id="9e66a-682">\I</span></span> | <span data-ttu-id="9e66a-683">\i 排除數字 (不支援) VIM</span><span class="sxs-lookup"><span data-stu-id="9e66a-683">\i except digits (NOT SUPPORTED) VIM</span></span> |
| <span data-ttu-id="9e66a-684">\k</span><span class="sxs-lookup"><span data-stu-id="9e66a-684">\k</span></span> | <span data-ttu-id="9e66a-685">關鍵字字元 FF (不支援) VIM</span><span class="sxs-lookup"><span data-stu-id="9e66a-685">keyword character (NOT SUPPORTED) VIM</span></span> |
| <span data-ttu-id="9e66a-686">\K</span><span class="sxs-lookup"><span data-stu-id="9e66a-686">\K</span></span> | <span data-ttu-id="9e66a-687">\k 排除數字 (不支援) VIM</span><span class="sxs-lookup"><span data-stu-id="9e66a-687">\k except digits (NOT SUPPORTED) VIM</span></span> |
| <span data-ttu-id="9e66a-688">\f</span><span class="sxs-lookup"><span data-stu-id="9e66a-688">\f</span></span> | <span data-ttu-id="9e66a-689">檔案名字元 (不支援) VIM</span><span class="sxs-lookup"><span data-stu-id="9e66a-689">file name character (NOT SUPPORTED) VIM</span></span> |
| <span data-ttu-id="9e66a-690">\F</span><span class="sxs-lookup"><span data-stu-id="9e66a-690">\F</span></span> | <span data-ttu-id="9e66a-691">\f 排除數字 (不支援) VIM</span><span class="sxs-lookup"><span data-stu-id="9e66a-691">\f except digits (NOT SUPPORTED) VIM</span></span> |
| <span data-ttu-id="9e66a-692">\p</span><span class="sxs-lookup"><span data-stu-id="9e66a-692">\p</span></span> | <span data-ttu-id="9e66a-693">可列印字元 (不支援) VIM</span><span class="sxs-lookup"><span data-stu-id="9e66a-693">printable character (NOT SUPPORTED) VIM</span></span> |
| <span data-ttu-id="9e66a-694">\P</span><span class="sxs-lookup"><span data-stu-id="9e66a-694">\P</span></span> | <span data-ttu-id="9e66a-695">\p 排除數字 (不支援) VIM</span><span class="sxs-lookup"><span data-stu-id="9e66a-695">\p except digits (NOT SUPPORTED) VIM</span></span> |
| <span data-ttu-id="9e66a-696">\s</span><span class="sxs-lookup"><span data-stu-id="9e66a-696">\s</span></span> | <span data-ttu-id="9e66a-697">空格字元 (≡ [\t]) (NOT SUPPORTED) VIM</span><span class="sxs-lookup"><span data-stu-id="9e66a-697">whitespace character (≡ [\t]) (NOT SUPPORTED) VIM</span></span> |
| <span data-ttu-id="9e66a-698">\S</span><span class="sxs-lookup"><span data-stu-id="9e66a-698">\S</span></span> | <span data-ttu-id="9e66a-699">非空格字元 (≡ [^ \t]) (NOT SUPPORTED) VIM</span><span class="sxs-lookup"><span data-stu-id="9e66a-699">non-white space character (≡ [^ \t]) (NOT SUPPORTED) VIM</span></span> |
| <span data-ttu-id="9e66a-700">\d</span><span class="sxs-lookup"><span data-stu-id="9e66a-700">\d</span></span> | <span data-ttu-id="9e66a-701">数位 (≡ [0-9]) VIM</span><span class="sxs-lookup"><span data-stu-id="9e66a-701">digits (≡ [0-9]) VIM</span></span> |
| <span data-ttu-id="9e66a-702">\D</span><span class="sxs-lookup"><span data-stu-id="9e66a-702">\D</span></span> | <span data-ttu-id="9e66a-703">非 \d VIM</span><span class="sxs-lookup"><span data-stu-id="9e66a-703">not \d VIM</span></span> |
| <span data-ttu-id="9e66a-704">\x</span><span class="sxs-lookup"><span data-stu-id="9e66a-704">\x</span></span> | <span data-ttu-id="9e66a-705">十六進位數位 (≡ [0-9A-Fa-f]) (NOT SUPPORTED) VIM</span><span class="sxs-lookup"><span data-stu-id="9e66a-705">hex digits (≡ [0-9A-Fa-f]) (NOT SUPPORTED) VIM</span></span> |
| <span data-ttu-id="9e66a-706">\X</span><span class="sxs-lookup"><span data-stu-id="9e66a-706">\X</span></span> | <span data-ttu-id="9e66a-707">非 \x (不支援) VIM</span><span class="sxs-lookup"><span data-stu-id="9e66a-707">not \x (NOT SUPPORTED) VIM</span></span> |
| <span data-ttu-id="9e66a-708">\o</span><span class="sxs-lookup"><span data-stu-id="9e66a-708">\o</span></span> | <span data-ttu-id="9e66a-709">八進位數位 (≡ [0-7]) (不支援) VIM</span><span class="sxs-lookup"><span data-stu-id="9e66a-709">octal digits (≡ [0-7]) (NOT SUPPORTED) VIM</span></span> |
| <span data-ttu-id="9e66a-710">\O</span><span class="sxs-lookup"><span data-stu-id="9e66a-710">\O</span></span> | <span data-ttu-id="9e66a-711">非 \o (不支援) VIM</span><span class="sxs-lookup"><span data-stu-id="9e66a-711">not \o (NOT SUPPORTED) VIM</span></span> |
| <span data-ttu-id="9e66a-712">\w</span><span class="sxs-lookup"><span data-stu-id="9e66a-712">\w</span></span> | <span data-ttu-id="9e66a-713">文字字元 VIM</span><span class="sxs-lookup"><span data-stu-id="9e66a-713">word character VIM</span></span> |
| <span data-ttu-id="9e66a-714">\W</span><span class="sxs-lookup"><span data-stu-id="9e66a-714">\W</span></span> | <span data-ttu-id="9e66a-715">非 \w VIM</span><span class="sxs-lookup"><span data-stu-id="9e66a-715">not \w VIM</span></span> |
| <span data-ttu-id="9e66a-716">\h</span><span class="sxs-lookup"><span data-stu-id="9e66a-716">\h</span></span> | <span data-ttu-id="9e66a-717">文字字元標題 FF (不支援) VIM</span><span class="sxs-lookup"><span data-stu-id="9e66a-717">head of word character (NOT SUPPORTED) VIM</span></span> |
| <span data-ttu-id="9e66a-718">\H</span><span class="sxs-lookup"><span data-stu-id="9e66a-718">\H</span></span> | <span data-ttu-id="9e66a-719">非 \h (不支援) VIM</span><span class="sxs-lookup"><span data-stu-id="9e66a-719">not \h (NOT SUPPORTED) VIM</span></span> |
| <span data-ttu-id="9e66a-720">\a</span><span class="sxs-lookup"><span data-stu-id="9e66a-720">\a</span></span> | <span data-ttu-id="9e66a-721">字母 \o (不支援) VIM</span><span class="sxs-lookup"><span data-stu-id="9e66a-721">alphabetic (NOT SUPPORTED) VIM</span></span> |
| <span data-ttu-id="9e66a-722">\A</span><span class="sxs-lookup"><span data-stu-id="9e66a-722">\A</span></span> | <span data-ttu-id="9e66a-723">非 \a (不支援) VIM</span><span class="sxs-lookup"><span data-stu-id="9e66a-723">not \a (NOT SUPPORTED) VIM</span></span> |
| <span data-ttu-id="9e66a-724">\l</span><span class="sxs-lookup"><span data-stu-id="9e66a-724">\l</span></span> | <span data-ttu-id="9e66a-725">小寫 (不支援)</span><span class="sxs-lookup"><span data-stu-id="9e66a-725">lowercase (NOT SUPPORTED) VIM</span></span> |
| <span data-ttu-id="9e66a-726">\L</span><span class="sxs-lookup"><span data-stu-id="9e66a-726">\L</span></span> | <span data-ttu-id="9e66a-727">非小寫 (不支援) VIM</span><span class="sxs-lookup"><span data-stu-id="9e66a-727">not lowercase (NOT SUPPORTED) VIM</span></span> |
| <span data-ttu-id="9e66a-728">\u</span><span class="sxs-lookup"><span data-stu-id="9e66a-728">\u</span></span> | <span data-ttu-id="9e66a-729">大寫 (不支援)</span><span class="sxs-lookup"><span data-stu-id="9e66a-729">uppercase (NOT SUPPORTED) VIM</span></span> |
| <span data-ttu-id="9e66a-730">\U</span><span class="sxs-lookup"><span data-stu-id="9e66a-730">\U</span></span> | <span data-ttu-id="9e66a-731">非大寫 (不支援) VIM</span><span class="sxs-lookup"><span data-stu-id="9e66a-731">not uppercase (NOT SUPPORTED) VIM</span></span> |
| <span data-ttu-id="9e66a-732">\_x</span><span class="sxs-lookup"><span data-stu-id="9e66a-732">\_x</span></span> | <span data-ttu-id="9e66a-733">\x 和分行符號，適用于任何 x (不支援) VIM</span><span class="sxs-lookup"><span data-stu-id="9e66a-733">\x plus newline, for any x (NOT SUPPORTED) VIM</span></span> |
| <span data-ttu-id="9e66a-734">\c</span><span class="sxs-lookup"><span data-stu-id="9e66a-734">\c</span></span> | <span data-ttu-id="9e66a-735">忽略大小寫 (不支援) VIM</span><span class="sxs-lookup"><span data-stu-id="9e66a-735">ignore case (NOT SUPPORTED) VIM</span></span> |
| <span data-ttu-id="9e66a-736">\C</span><span class="sxs-lookup"><span data-stu-id="9e66a-736">\C</span></span> | <span data-ttu-id="9e66a-737">符合大小寫 (不支援) VIM</span><span class="sxs-lookup"><span data-stu-id="9e66a-737">match case (NOT SUPPORTED) VIM</span></span> |
| <span data-ttu-id="9e66a-738">\m</span><span class="sxs-lookup"><span data-stu-id="9e66a-738">\m</span></span> | <span data-ttu-id="9e66a-739">魔術 (不支援) VIM</span><span class="sxs-lookup"><span data-stu-id="9e66a-739">magic (NOT SUPPORTED) VIM</span></span> |
| <span data-ttu-id="9e66a-740">\M</span><span class="sxs-lookup"><span data-stu-id="9e66a-740">\M</span></span> | <span data-ttu-id="9e66a-741">非魔術 (不支援) VIM</span><span class="sxs-lookup"><span data-stu-id="9e66a-741">nomagic (NOT SUPPORTED) VIM</span></span> |
| <span data-ttu-id="9e66a-742">\v</span><span class="sxs-lookup"><span data-stu-id="9e66a-742">\v</span></span> | <span data-ttu-id="9e66a-743">超魔術 (不支援) VIM</span><span class="sxs-lookup"><span data-stu-id="9e66a-743">verymagic (NOT SUPPORTED) VIM</span></span> |
| <span data-ttu-id="9e66a-744">\V</span><span class="sxs-lookup"><span data-stu-id="9e66a-744">\V</span></span> | <span data-ttu-id="9e66a-745">超非魔術 (不支援) VIM</span><span class="sxs-lookup"><span data-stu-id="9e66a-745">verynomagic (NOT SUPPORTED) VIM</span></span> |
| <span data-ttu-id="9e66a-746">\Z</span><span class="sxs-lookup"><span data-stu-id="9e66a-746">\Z</span></span> | <span data-ttu-id="9e66a-747">忽略 Unicode 結合字元中的差異 (不支援) VIM</span><span class="sxs-lookup"><span data-stu-id="9e66a-747">ignore differences in Unicode combining characters (NOT SUPPORTED) VIM</span></span> |

|  | <span data-ttu-id="9e66a-748">魔術</span><span class="sxs-lookup"><span data-stu-id="9e66a-748">Magic</span></span> |
| --- | --- |
| <span data-ttu-id="9e66a-749">(?{code})</span><span class="sxs-lookup"><span data-stu-id="9e66a-749">(?{code})</span></span> | <span data-ttu-id="9e66a-750">任意 Perl 代碼 (不支援) PERL</span><span class="sxs-lookup"><span data-stu-id="9e66a-750">arbitrary Perl code (NOT SUPPORTED) PERL</span></span> |
| <span data-ttu-id="9e66a-751">(??{code})</span><span class="sxs-lookup"><span data-stu-id="9e66a-751">(??{code})</span></span> | <span data-ttu-id="9e66a-752">已延遲任意 Perl 代碼 (不支援) PERL</span><span class="sxs-lookup"><span data-stu-id="9e66a-752">postponed arbitrary Perl code (NOT SUPPORTED) PERL</span></span> |
| <span data-ttu-id="9e66a-753">(?n)</span><span class="sxs-lookup"><span data-stu-id="9e66a-753">(?n)</span></span> | <span data-ttu-id="9e66a-754">對 regexp 擷取群組 n 的遞迴撥號 (不支援)</span><span class="sxs-lookup"><span data-stu-id="9e66a-754">recursive call to regexp capturing group n (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="9e66a-755">(?+n)</span><span class="sxs-lookup"><span data-stu-id="9e66a-755">(?+n)</span></span> | <span data-ttu-id="9e66a-756">遞迴呼叫相關群組 +n (不支援)</span><span class="sxs-lookup"><span data-stu-id="9e66a-756">recursive call to relative group +n (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="9e66a-757">(?-n)</span><span class="sxs-lookup"><span data-stu-id="9e66a-757">(?-n)</span></span> | <span data-ttu-id="9e66a-758">遞迴呼叫相關群組 -n (不支援)</span><span class="sxs-lookup"><span data-stu-id="9e66a-758">recursive call to relative group -n (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="9e66a-759">(?C)</span><span class="sxs-lookup"><span data-stu-id="9e66a-759">(?C)</span></span> | <span data-ttu-id="9e66a-760">PCRE 圖說文字 (不支援) PCRE</span><span class="sxs-lookup"><span data-stu-id="9e66a-760">PCRE callout (NOT SUPPORTED) PCRE</span></span> |
| <span data-ttu-id="9e66a-761">(?R)</span><span class="sxs-lookup"><span data-stu-id="9e66a-761">(?R)</span></span> | <span data-ttu-id="9e66a-762">對整個 regexp 的遞迴撥號 (≡ (?0)) (不支援)</span><span class="sxs-lookup"><span data-stu-id="9e66a-762">recursive call to entire regexp (≡ (?0)) (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="9e66a-763">(?&amp;name)</span><span class="sxs-lookup"><span data-stu-id="9e66a-763">(?&amp;name)</span></span> | <span data-ttu-id="9e66a-764">遞迴呼叫具名群組 (不支援)</span><span class="sxs-lookup"><span data-stu-id="9e66a-764">recursive call to named group (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="9e66a-765">(?P=name)</span><span class="sxs-lookup"><span data-stu-id="9e66a-765">(?P=name)</span></span> | <span data-ttu-id="9e66a-766">具名反向參考 (不支援)</span><span class="sxs-lookup"><span data-stu-id="9e66a-766">named backreference (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="9e66a-767">(?P&gt;name)</span><span class="sxs-lookup"><span data-stu-id="9e66a-767">(?P&gt;name)</span></span> | <span data-ttu-id="9e66a-768">遞迴呼叫具名群組 (不支援)</span><span class="sxs-lookup"><span data-stu-id="9e66a-768">recursive call to named group (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="9e66a-769">(?(cond)true</span><span class="sxs-lookup"><span data-stu-id="9e66a-769">(?(cond)true</span></span>|<span data-ttu-id="9e66a-770">false)</span><span class="sxs-lookup"><span data-stu-id="9e66a-770">false)</span></span> | <span data-ttu-id="9e66a-771">條件式分支 (不支援)</span><span class="sxs-lookup"><span data-stu-id="9e66a-771">conditional branch (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="9e66a-772">(?(cond)true)</span><span class="sxs-lookup"><span data-stu-id="9e66a-772">(?(cond)true)</span></span> | <span data-ttu-id="9e66a-773">條件式分支 (不支援)</span><span class="sxs-lookup"><span data-stu-id="9e66a-773">conditional branch (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="9e66a-774">(\*ACCEPT)</span><span class="sxs-lookup"><span data-stu-id="9e66a-774">(\*ACCEPT)</span></span> | <span data-ttu-id="9e66a-775">讓 regexps 更像 Prolog (不支援)</span><span class="sxs-lookup"><span data-stu-id="9e66a-775">make regexps more like Prolog (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="9e66a-776">(\*COMMIT)</span><span class="sxs-lookup"><span data-stu-id="9e66a-776">(\*COMMIT)</span></span> | <span data-ttu-id="9e66a-777">(不支援)</span><span class="sxs-lookup"><span data-stu-id="9e66a-777">(NOT SUPPORTED)</span></span> |
| <span data-ttu-id="9e66a-778">(\*F)</span><span class="sxs-lookup"><span data-stu-id="9e66a-778">(\*F)</span></span> | <span data-ttu-id="9e66a-779">(不支援)</span><span class="sxs-lookup"><span data-stu-id="9e66a-779">(NOT SUPPORTED)</span></span> |
| <span data-ttu-id="9e66a-780">(\*FAIL)</span><span class="sxs-lookup"><span data-stu-id="9e66a-780">(\*FAIL)</span></span> | <span data-ttu-id="9e66a-781">(不支援)</span><span class="sxs-lookup"><span data-stu-id="9e66a-781">(NOT SUPPORTED)</span></span> |
| <span data-ttu-id="9e66a-782">(\*MARK)</span><span class="sxs-lookup"><span data-stu-id="9e66a-782">(\*MARK)</span></span> | <span data-ttu-id="9e66a-783">(不支援)</span><span class="sxs-lookup"><span data-stu-id="9e66a-783">(NOT SUPPORTED)</span></span> |
| <span data-ttu-id="9e66a-784">(\*PRUNE)</span><span class="sxs-lookup"><span data-stu-id="9e66a-784">(\*PRUNE)</span></span> | <span data-ttu-id="9e66a-785">(不支援)</span><span class="sxs-lookup"><span data-stu-id="9e66a-785">(NOT SUPPORTED)</span></span> |
| <span data-ttu-id="9e66a-786">(\*SKIP)</span><span class="sxs-lookup"><span data-stu-id="9e66a-786">(\*SKIP)</span></span> | <span data-ttu-id="9e66a-787">(不支援)</span><span class="sxs-lookup"><span data-stu-id="9e66a-787">(NOT SUPPORTED)</span></span> |
| <span data-ttu-id="9e66a-788">(\*THEN)</span><span class="sxs-lookup"><span data-stu-id="9e66a-788">(\*THEN)</span></span> | <span data-ttu-id="9e66a-789">(不支援)</span><span class="sxs-lookup"><span data-stu-id="9e66a-789">(NOT SUPPORTED)</span></span> |
| <span data-ttu-id="9e66a-790">(\*ANY)</span><span class="sxs-lookup"><span data-stu-id="9e66a-790">(\*ANY)</span></span> | <span data-ttu-id="9e66a-791">設定分行符號慣例 (不支援)</span><span class="sxs-lookup"><span data-stu-id="9e66a-791">set newline convention (NOT SUPPORTED)</span></span> |
| <span data-ttu-id="9e66a-792">(\*ANYCRLF)</span><span class="sxs-lookup"><span data-stu-id="9e66a-792">(\*ANYCRLF)</span></span> | <span data-ttu-id="9e66a-793">(不支援)</span><span class="sxs-lookup"><span data-stu-id="9e66a-793">(NOT SUPPORTED)</span></span> |
| <span data-ttu-id="9e66a-794">(\*CR)</span><span class="sxs-lookup"><span data-stu-id="9e66a-794">(\*CR)</span></span> | <span data-ttu-id="9e66a-795">(不支援)</span><span class="sxs-lookup"><span data-stu-id="9e66a-795">(NOT SUPPORTED)</span></span> |
| <span data-ttu-id="9e66a-796">(\*CRLF)</span><span class="sxs-lookup"><span data-stu-id="9e66a-796">(\*CRLF)</span></span> | <span data-ttu-id="9e66a-797">(不支援)</span><span class="sxs-lookup"><span data-stu-id="9e66a-797">(NOT SUPPORTED)</span></span> |
| <span data-ttu-id="9e66a-798">(\*LF)</span><span class="sxs-lookup"><span data-stu-id="9e66a-798">(\*LF)</span></span> | <span data-ttu-id="9e66a-799">(不支援)</span><span class="sxs-lookup"><span data-stu-id="9e66a-799">(NOT SUPPORTED)</span></span> |
| <span data-ttu-id="9e66a-800">(\*BSR\_ANYCRLF)</span><span class="sxs-lookup"><span data-stu-id="9e66a-800">(\*BSR\_ANYCRLF)</span></span> | <span data-ttu-id="9e66a-801">設定 \R 慣例 (不支援) PCRE</span><span class="sxs-lookup"><span data-stu-id="9e66a-801">set \R convention (NOT SUPPORTED) PCRE</span></span> |
| <span data-ttu-id="9e66a-802">(\*BSR\_UNICODE)</span><span class="sxs-lookup"><span data-stu-id="9e66a-802">(\*BSR\_UNICODE)</span></span> | <span data-ttu-id="9e66a-803">(不支援) PCRE</span><span class="sxs-lookup"><span data-stu-id="9e66a-803">(NOT SUPPORTED) PCRE</span></span> |

## <span data-ttu-id="9e66a-804">內容授權</span><span class="sxs-lookup"><span data-stu-id="9e66a-804">Content license</span></span>

> [!NOTE]
> <span data-ttu-id="9e66a-805">本頁的某些部分是根據 Chromium.org 創造和分享的作品加以修改，並根據[創用 CC 姓名標示 4.0 國際版本授權條款](http://creativecommons.org/licenses/by/4.0/)中所述條款加以使用。</span><span class="sxs-lookup"><span data-stu-id="9e66a-805">Portions of this page are modifications based on work created and shared by Chromium.org and used according to terms described in the [Creative Commons Attribution 4.0 International License](http://creativecommons.org/licenses/by/4.0/).</span></span> <span data-ttu-id="9e66a-806">原始頁面可在[此處](https://github.com/google/re2/wiki/Syntax)找到。</span><span class="sxs-lookup"><span data-stu-id="9e66a-806">The original page can be found [here](https://github.com/google/re2/wiki/Syntax).</span></span>
  
<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br /><span data-ttu-id="9e66a-807">本作品根據<a rel="license" href="http://creativecommons.org/licenses/by/4.0/">創用 CC 姓名標示 4.0 國際版本授權條款</a>獲得授權。</span><span class="sxs-lookup"><span data-stu-id="9e66a-807">This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.</span></span>

## <span data-ttu-id="9e66a-808">請參閱</span><span class="sxs-lookup"><span data-stu-id="9e66a-808">See also</span></span>

- [<span data-ttu-id="9e66a-809">Microsoft Edge 企業登陸頁面</span><span class="sxs-lookup"><span data-stu-id="9e66a-809">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)